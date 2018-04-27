# Demo
[Demo of this application (hosted on Heroku)](https://quiet-reaches-30094.herokuapp.com/)

# Install and Run

## Add Firebase config
The app is setup to use two instances of Firebase, one for development/production and one for test.

1. Create a new Firebase instance at [firebase.google.com/](https://firebase.google.com/).
2. Create a new file at the root of the app called `.env.development`
3. Copy the following into the file:
```
FIREBASE_API_KEY=
FIREBASE_AUTH_DOMAIN=
FIREBASE_DATABASE_URL=
FIREBASE_PROJECT_ID=
FIREBASE_STORAGE_BUCKET=
FIREBASE_MESSAGING_SENDER_ID=
```
4. On the Firebase **Project Overview** page, click on **Add Firebase to your web app**
5. Copy the relevant details into the `.env.development` file. Do not use any quotes or spaces. The file should resemble the below:
```
FIREBASE_API_KEY=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
FIREBASE_AUTH_DOMAIN=my-app.firebaseapp.com
FIREBASE_DATABASE_URL=https://my-app.firebaseio.com
FIREBASE_PROJECT_ID=my-app
FIREBASE_STORAGE_BUCKET=my-app.appspot.com
FIREBASE_MESSAGING_SENDER_ID=123456789234
```
6. Save `.env.development`
7. To run the unit tests, create the `.env.test` file and repeat the steps above with a separate Firebase instance. This step is only required if you want to run the unit tests, it is not necessary to run the app.
8. It should now be possible to install and run the app. You can log in to the Firebase console to see the expenses as you add, edit and delete them.

## Run the app
`yarn install`

`yarn run dev-server` starts a development server on [localhost:8080/](http://localhost:8080/)

## Unit tests
`yarn run test`
