---
order: 1
title: What Version of This Blog Do You See?
---

As you can see, this website does not have a formal version tag. It tries to use the latest version of `ng-zorro-antd` and Angular as some kind of version tag. So, just imagine how surprised I was when I deployed this website compiled with Angular `^12.2.9` and checking my very old Samsung that runs on Android 4.4.2. For some reason, the old Chrome web browser does not want to load this website correctly, so, I use an old version of FireFox browser for Android (As you may know, Google does not allow to update apps for old Android versions.) FireFox worked ok at first. But, when I closed and opened the browser again, this site loaded automatically and showed Angular `^12.2.4` at the bottom of the footer. Somehow, FireFox cached an old version of my website. Deleting the FireFox cache did not help, but, reloading the URL would show the correct Angular `^12.2.9`.

## The Problem

It may be problematic to have latest version for some websites that use Angular. Imagine a user browsing your website just seconds before you stat to deploy a new version of your website. The user will still have the old version of you website (old Angular compiled JavaScript files) even after the deployment ends.

## The Solution

The most simple solution is to let your users know that a new version of your website is available and ask them to refresh the webpage. It was very simple for me to implement this solution because I use a server-side API and deploy my back end and front end on the same server and generate my deployment with a Node.js script. So, I generate a small PHP file and small TypeScript file with some unique hash.

```php
<?php
namespace Acioina\UserManagement\Http\Controllers\Api;
use Acioina\UserManagement\Transformers\VersionTransformer;

class VersionController extends ApiController
{
    private const ANGULAR_APP_HASH = 'b607b9112d721b487e78121fc3bbf455';

    public function __construct(VersionTransformer $transformer)
    {
        parent::__construct($transformer);
    }

    public function index()
    {
        return $this->respondWithTransformer(['hash' => self::ANGULAR_APP_HASH]);
    }
}
```

```typescript
export const APP_VERSION = {
  version: '0.0.0',
  hash: 'b607b9112d721b487e78121fc3bbf455',
};
```

In my `app.component.ts`, I have something like this:

```typescript
@Component({
  selector: 'app-root',
  template: `
    <div class="page-wrapper">
      <app-header [windowWidth]="windowWidth" [isLoggedIn]="isLoggedIn" [username]="username"> </app-header>
      <ng-container *ngIf="notification">
        <nz-card>
          <div nz-row nzJustify="center">
            <div nz-col>
              <h5 nz-typography nzType="danger" [nzContent]="notification"></h5>
            </div>
          </div>
        </nz-card>
      </ng-container>
...
`
  ngOnInit(): void {
    this.versionFacade.getVersion();

    this.versionFacade.versionHash$.pipe(takeUntil(this.destroy$)).subscribe((hash: string) => {
      if (hash && hash !== APP_VERSION.hash) {
        this.notification =
          'You are using an old version of this website and some pages may not work correctly. Please reload/refresh the page in order to load the latest version.';
        this.cdr.markForCheck();
      }
    });
  }
```

And I compile my front end app with a command like this: `yarn build:site`. If you want that your hash to have some meaning, you may use [this](https://medium.com/@amcdnl/version-stamping-your-app-with-the-angular-cli-d563284bb94d) idea.

Please read **gkalpak**'s answer [here](https://stackoverflow.com/questions/55494181/what-is-the-purpose-of-swupdate-activateupdate-in-angular/59175788#59175788) in order to implement a more complex solution.
