# auto-package-test

Went through steps outlined here: https://truechoice.atlassian.net/wiki/spaces/ENG/pages/1821966343/Guide+Publish+Release+Packages+using+Auto+CD+Workflow+included

v0.1.0 => Manually published initial package to GitHub Packages running `npm publish`
<br />
v0.2.0 => Second release was through `npx auto shipit` (minor + release labels)
<br />
v0.3.0 => Third release was through CD Workflow => triggered `npx auto shipit` (minor + release labels)

### For v0.2.0 & v0.3.0 releases (using **auto**) - verified they both output:

1. package.json version bump
2. git tag created locally + remotely
3. latest package version published (both releases had `minor` + `release` labels)
4. release created with reference to newest tag (#2)

### If you want to use this package inside another project:

`npm install @lyoon-tcs/auto-package-test@0.1.0`
<br />
index.js =>
<br />
`const package = require('@lyoon-tcs/auto-package-test');`
<br />
`console.log(package.getName('your-name'));`
