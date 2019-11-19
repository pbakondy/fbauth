# Simple Google authentication with Angular Firebase 

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.3.19.

## Initial Firebase Setup

- Open Firebase Console
- Create a new Project
- Navigate to Authentication / Sign-in method
- Enable Google provider (only) 

## Build project

```
ng new fbauth
cd fbauth

npm install @angular/fire firebase --save

ng generate service services/auth
ng generate component components/index
ng generate component components/user-profile
ng generate guard guards/auth
```

- edit `app.module.ts` to initialize firebase settings
- edit `app-routing.module.ts` to add routing rules
- edit `user-profile.component.ts` and `user-profile.component.html` to setup Google login
- edit `auth.guard.ts` to implement permission check for routes

## Restrict by user

Google authentication handles only the login process.

You can restrict access (authorization) only by Firebase access rules: Firebase Console / Database / Rules . 

## Resources

- https://fireship.io/lessons/angularfire-google-oauth/
- https://stackoverflow.com/a/28422909

