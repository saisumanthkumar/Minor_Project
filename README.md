# Minor_Project
Student Mantras is a react based web application for listing various opportunities. 
To deploy this app on localhost:<br />
In the project directory, you can run:<br />

#### npm start<br />
Runs the app in the development mode.<br />
Open http://localhost:3000 to view it in the browser.<br />

The page will reload if you make edits.<br />
You will also see any lint errors in the console.<br />

#### npm run build<br />
Builds the app for production to the build folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.<br />

App is ready to be deployed!
const githubAPI = "https://api.github.com"
const commitsEndpoint = "/repos/csitauthority/CSITauthority.github.io/commits"
const commitsURL = githubAPI + commitsEndpoint
const filepath = "HUGO/content/post/vlan-101.md"
fetch(commitsURL + "?path=" + filepath)
  .then(response => response.json())
  .then(commits => {
    for (var i = 0; i < commits.length; i++) {
      console.log(commits[i].commit.author.name)
    }
  })
