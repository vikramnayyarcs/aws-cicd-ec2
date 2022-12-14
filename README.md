# AWS EC2 CICD

This repo contains a basic React app which I can use to setup a CI/CD pipeline with AWS.

Check out the description for a link to the tutorial.
https://www.youtube.com/watch?v=0Kn6mAYIRJU&t=323s

## Steps:
Code the project however you want and push to a repo.

### Create AWS EC2 instance:

  Name
  
  Ubuntu OS
  
  Generate new key pair (pem, directory matters!)
  
  Create Security Group
  
  Allow internet traffic (HTTP & HTTPS)
  
  **Launch Instance**
  
GitHub Settings:
  Actions->Runners. 'New self-hosted runners'.
  
  Follow steps, using Linux OS (instance OS).
  
### Connect to instance using SSH Client (copy paste command):
  
   Create a new directory.
   
   Paste in commands (Validate hash, extract hash using tar*, enter). -> 'Runner added successfully'.
   
   sudo ./svc.sh install
   
   sudo ./svc.sh

   Refresh and should see IP.
   
  ### GitHub Actions:
  Select Node JS.
  
  Remove PR part.
  
  Line 13: runs-on: self-hosted
  
  Node version changes* (remove others)
  
  Remove test cases if none
  
  Start commit
  
  Refresh and should see runners (change npm ci to npm i if fails).
   
### Go to Instance Inside of Newly Created Directory:
sudo apt install nginx (If successful, public IPV4 DNS will be available when selecting your instance, not yet usable,https will succeed).

ls ; cd _work ; ls (repositiory name) cd repo name, ls (build) , cd build, ls (index.html).

Copy path of index.html (pwd, save for later).

### Update Nginx Settings:
From /build, cd /etc/nginx

cd sites-available

sudo rm default

sudo nano default

Paste in script (fill in root path from earlier).

sudo service nginx restart

Internal server error (temporary).

chmod +x (build folder path iteratively).

./1

./1/2

./1/2/3


   

# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
