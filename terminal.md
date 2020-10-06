# Terminal Cheatsheet

### Simple Commands:

`cd`: Change directory

`ls`: List the contents of a directory

`mkdir`: Make a directory

`touch fileName`: Make a file called "fileName"

### npm:

`npm install -g [package-name]`: install the "package-name" package (-g means global). May need to use `sudo` to 
override restrictions

`npm install --save [package-name]`: install the "package-name" package to project folder

`npm start`: start project

`ctrl + c`: stop project

`npm run build`: build app (any changes made must use this to update)

### Firebase Deploy:

`firebase login` to login

`firebase init`  to initialize (set your "public" directory to "build" in the questions).
Also make sure to NOT overwrite your index.html

`firebase deploy` to deploy your app!

`create-react-app` always puts built app in the `build` folder, so when setting up Firebase, remember to type "build" in 
the question about "where is your public directory located?"
