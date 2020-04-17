# Angular Dynamic Routes

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 6.0.3.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).




https://angular-firebase-hosting-c622d.firebaseapp.com/home


# How to install this project?

ng build --prod --output-path angularapp

npm install -g firebase-tools

firebase login

firebase init

The list of questions Firebase tools will ask:

? Are you ready to proceed? Yes
Which Firebase CLI features do you want to setup for this folder? Press Space to select features, then Enter to confirm your choices.
( ) Database: Deploy Firebase Realtime Database Rules
( ) Firestore: Deploy rules and create indexes for Firestore
( ) Functions: Configure and deploy Cloud Functions
>(*) Hosting: Configure and deploy Firebase Hosting sites
( ) Storage: Deploy Cloud Storage security rules
? Select a default Firebase project for this directory:
[create a new project]
[don’t setup a default project]
> grokonez-angulardeploy (AngularDeploy)
jsa-cloud-firestore (JSA Cloud Firestore)
jsa-firebaseauth-6d45a (JSA FirebaseAuth)
(Move up and down to reveal more choices)
? What do you want to use as your public directory? (public) angularapp
? Configure as a single-page app (rewrite all urls to /index.html)? (y/N) y
? File angularapp/index.html already exists. Overwrite? No



-> Firebase CLI will create 2 files for linking:

– .firebaserc file -> Sets the Firebase project we’re linking to :

{
  "projects": {
    "default": "grokonez-angulardeploy"
  }
}
– firebase.json -> Sets the deployed folder and rewrites :

{
  "hosting": {
    "public": "angularapp",
    "ignore": [
      "firebase.json",
      "**/.*",
      "**/node_modules/**"
    ],
    "rewrites": [
      {
        "source": "**",
        "destination": "/index.html"
      }
    ]
  }
}

firebase deploy



#Re-Deployment

Open the package.json file, then add a new script as below:

"scripts": {
  ...
  "deploy": "ng build --prod --output-path angularapp && firebase deploy"
},

npm run deploy

