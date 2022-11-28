## Al-Khattaba Admin

Al-Khattaba Admin is a User Interface framework used by Alkhattaba employees to allow communication between Al-khattaba employees and Al-khattaba servers.

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).


## Table Of Content
* [SRC Structure](#src-structure)
* [Admin UI menu bar categories](#admin-ui-menu-bar-categories)
* [Installation](#installation)
* [Available Scripts](#available-scripts)
* [API reference](#api-reference)
* [Learn More](#learn-more)

## SRC Structure
* ### `Assets/Images`
Assets/images used in admin UI.
* ### `Components`
  * The static part the render what is required from stores
  * Read logic from stores
  * Use core elements to render what is required
  * Seperated to two parts
     * Desktop : render that appears on any pc screen
     * Mobile : render that appears on mobile devices
* ### `Configuration`
Folder containing all the configuration of the three differnet modes : staging, production, development.
* ### `Constants`
Folder containing all the static constant used in Admin UI.
* ### `Helpers`
Utilities used in the client admin side.
* ### `Routes`
Routes used in the client admin side.
* ### `Stores`
  * The mobX stores where all the logic happen
  * The components only render what these stores tell them to render
* ### `Styles`
Css styles used in admin UI.
* ### `api`
Admin API calls between client and server.
* ### `core`
The base of the client admin:
  * i18n : all cw in the app are here. text cant be added staticly to components
  * theme : color, fonts, font size, line height and languages are only imported from here
  * elements : the shared elements used 
* ### `react-app-env.d.ts`
This file references TypeScript types declarations that are specific to projects started with Create React App.
These type declarations add support for importing resource files such as bmp, gif, jpeg, jpg, png, webp, and svg.
* ### `serviceWorker.js`
This is optional code is used to register a service worker.

## Admin UI menu bar categories
### `Welcome Page`
welcome page for the logged in user, ex: WELCOME: Username

### `Alarms`
* alarms: list all the alarms related to (website & application) 
* on call table: list on call (se & qa) employees who are on call duty, and the CET plus CTO with information to contact them.

### `Approve/Reject data`
* Get Approve or Reject on user pictures and description
* Clean Pool.

### `Reports`
* Get Reports from user to another
* Clean Pool.

### `Investigation Cases`
* Get Investigation Cases.

### `User`
The needed information for/about users.
* #### 1- Advanced: get user advanced mode
* #### 2- Conversations: get user conversation between 2 users
* #### 3- Devices: search advance mode by the Device ID
* #### 4- Edit profile: search Edit profile by the User ID
* #### 5- Events: search monitor user events by the User ID
* #### 6- Login: search monitor user login by the User ID
* #### 7- Messages: search monitor user messages by the User ID
* #### 8- Message Id: search monitor user messages by message ID
* #### 9- Payments: search by user id & by transaction id
* #### 10- Referral Code Usage: to get the User Referral Code Usage
* #### 11- Promo Code Usage: to get the Promo Code Usage

### `CSR`
The needed information for/about CSR.
* #### 1- Change Password
* #### 2- My CSR Performance
* #### 3- My CSR Mistakes
* #### 4- My CSR Prev Actions

### `Auditor`
The needed information for/about auditors.
* #### 1- Audit: view/audit admin events
* #### 2- Audited Events: view admin events Audited
* #### 3- My Auditing Performance: get My Auditing Performance
* #### 4- My Auditing Mistakes: get My Auditing Mistakes
* #### 5- Other CSRs Performance: get Other CSRs Performance
* #### 6- Events Chart: view admin events charts
* #### 7- Pool: view/edit admin pool
* #### 8- T.B.W Reasons: get Temporary Ban , Ban , Warn Reasons / add TBW
* #### 9- Workload Data: get Workload data between two dates
* #### 10- Promo Code
  * Generate: Generate Promo Code
  * Get: get All Promo Codes
  * Edit: Update Promo Code
  * Get: get Promo Code Usage

### `Supervisor`
The needed information for/about supervisors.
* #### 1- Permission: view/edit admin permission
* #### 2- Supervise: Supervise Admin Audits
* #### 3- Supervised Events: View Supervised Audit Events

### `Developer`
The needed information for/about developers.
* #### 1- Flagged Connections: to get Flagged Connections Dashboard
* #### 2- On Call: to get On Call Dashboard
* #### 3- VIP Issues: search User Latest Receipt using userID & platform
* #### 4- Watch Alerts: get Watch Alert Dashboard in line Graphs for:
  * User
  * Users Login
  * Users Payments
* #### 5- Flush: In order to press the Flush hosts we need Email, Password and Pass Code
  ##### note: it is danger to press.

### `Shareholder`
* Get Shareholders Update: to get the shareholder by Date Range.

panel charts for `Total Users`, `New Users`, `Total Conversations`, `New Conversations`, `Total Messages`, `New Messages`, `Sales (USD)` & `Marketing Expenses (USD)`


## Installation

run the below code to download all the modules needed:
```bash
yarn
```

### Available Scripts

In the project directory, you can run:
 * run the below command so the script generates the required files and folders to start the React application and run it on the browser. This allows you to focus on coding your application without having to bother with build configurations.
```bash
yarn start
```
 * run the below command to starts a TypeScript compiler with --watch parameter, with the ability to react to compilation status. tsc-watch was created to allow an easy dev process with TypeScript. Commonly used to restart a node server, similar to nodemon but for TypeScript. Executes COMMAND on every successful compilation.
```bash
yarn watch
```
 * run the below command to launch the code in development mode:
```bash
yarn config-development
```
 * run the below command to launch the code in staging mode:
```bash
yarn config-staging 
```
 * run the below command to launch the code in production mode:
```bash
yarn config-production 
```
 * run the below command to generates all of your build artifacts but does no optimization of them (and does not define the “production” environment in Node, which some packages will look for and respond to).
```bash
yarn build
```
 * run the below command so you can use react-scripts to write unit tests without setting up a build process with Babel and Webpack/Rollup. It's useful when you want to quickly test an idea, but you're not sure if you want to create a library yet. It can also be useful when your code lives inside a yarn workspace and doesn't need a build process.
```bash
yarn test
```
 * run the below command to removes Create React App scripts and preset configurations and copies build dependencies, configuration files, and scripts into the app directory. If you do this, you can't go back to using Create React App on your project!
**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

```bash
yarn eject
```
 * run the below command to open index.js in the deploy folder "node ./deploy/index.js":
```bash
yarn deploy
```
 * run the below command to open index.js in the git-helper folder "node ./git-helper/index.js":
```bash
yarn active-branch
```

<a name="api-reference"></a>
## API reference
Localhost API: [Localhost](http://localhost:3000)

Admin Staging API: [staging](https://admin-staging.alkhattaba.app/).

Admin Development API: [development](https://admin-production.alkhattaba.app/)

<a name="learn-more"></a>
## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

#### [Code Splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

#### [Analyzing the Bundle Size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

#### [Making a Progressive Web App](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

#### [Advanced Configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

#### [Deployment](https://facebook.github.io/create-react-app/docs/deployment)

#### [yarn build fails to minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
