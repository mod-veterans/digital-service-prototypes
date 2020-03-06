## Getting the code
 
#### Create Documents/Stash directory
 
#### Open Terminal

```
cd ~/Documents/Stash/
 
git clone https://stash.customappsteam.co.uk/scm/modvets/govuk-veterans-prototypes.git
 ```
 
 
 <br />  
     
## Making Changes
 
Here, you will want to work as normal – create, edit delete files etc, but Git will be tracking all the changes that you make. Once you reach a logical checkpoint and want to save your progress, do the following:
 
#### Open Terminal
 
 ```
cd ~/Documents/Stash/govuk-veterans-prototypes/
 
git status  // this will show you the files that have changed
 
git add .   // this will add all new files to the commit
 
git commit -m “Provide a short message explaining what you have done in this commit”
 
git push    // this will sync your local changes to the remote repository
 ```
 
  <br />  
    
## Getting the latest version
 
If someone else has made changes, your local version will be out of date. In this case, you will need to pull the latest version.
 
#### Open Terminal
 
```
cd ~/Documents/Stash/govuk-veterans-prototypes/
 
git pull
```
 
 <br />  

## Deployment
We use Heroku to deploy the app.

The link is: https://afcs-template.herokuapp.com/ and you will need a username and password to access the site.

Ensure you have the Heroku CLI installed, and a Heroku account, if you don't do the following:

```
brew tap heroku/brew && brew install heroku
```

Create an account here: https://signup.heroku.com/

To deploy the app...

#### Open Terminal

```
heroku login

cd ~/Documents/Stash/govuk-veterans-prototypes/
 
heroku git:remote -a afcs-template

git push heroku master
```