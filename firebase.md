###Deploy React App

1. `npm run build`: build app (any changes made must use this to update)

2. Create project on Firebase

3a. `firebase login` to login
   
3b. `firebase init`  to initialize (set your "public" directory to "build" in the questions).
   Also make sure to NOT overwrite your index.html
   
4. Choose "hosting" option only

5. Select  "Use an existing project"

6. For the "public directory" question, enter "build"

7. For the "single-page-app" question, enter "y"

8. File "build/index.html already exists" question, enter "n"

9. `firebase deploy` to deploy your app!

###Pushing Changes to Firebase App

1. `npm run build`: build app (any changes made must use this to update)

2. `firebase deploy` to deploy your app!