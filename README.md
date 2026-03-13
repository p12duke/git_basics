# Github basics


## Installation  

### On linux :
> sudo apt install  git gh

### On Windows/Mac os : 
- Manually install a github cli


# Initial setup and configurations

- Considering the host system to be a linux distro


### setup login 
> git config --global user.name
> git config --global user.password



NOTE: --global will setup all credential on global level. You can also setup a different scope based on your requirements and projects.


### Setup ssh 

- Read this excellent guide for setting up  your ssh server on linux distro.
  [ Hostman: setting up an ssh server] [https://hostman.com/tutorials/how-to-install-and-configure-ssh-on-ubuntu-22-04/#step-6-optional--create-key-pair-for-secure-authentication]

  [ Ubuntu-server_community: setting up an ssh]
  [https://ubuntu.com/server/docs/how-to/security/openssh-server/]

- Once you're done with your ssh setup you will need to setup an ssh keygen for your github account : 


  1. Go to the github website
  2. Login into your shell and open settings
  3. Go to ssh and GPG keys
  4. Create an ssh key using the New ssh key button
  5. Copy your entire ssh key from the ssh generated key in ( ~/.ssh/) folder which          you've created earlier and paste it in the text area of key tag.
  6. Done!
 
  - You're now having an account setup with ssh key.


  ### Steps to login and test  your Github connection.

    1. Eval the ssh key gen using this command
       ``` eval "$(ssh-agent -s) ```
       This should show a pid for your ssh-agent.
    2. Use the following command to test your connection :
       > ssh -t git@github.com
       If you receive an error, then you need to ensure that correct
       key was generated using this command
        ssh-keygen -t <algo> -C "gitusername@github.com"
       Make sure to edit the algo with your fav algo for keygen and your gitusername.



  ### Testing Authentication with github cli

    Github cli is an essential tool to manage your repositories and perform
    actions on your repo that is not possible with git commands due to leverage
    of permissions.

     To work with github cli

     We should first ideally check the auth and verify the ssh or the https:login credential using this command
      > gh auth login

      You would be prompted to enter into the github -web ui and verify the code  prompted.



### Basic Working of Github
Github is a hub or container for your all of your repositories on internet. 
Repository is a remote folder ( in basic terms) that can have multiple branches
which are basically in simple terms can be concluded as an image of your work/project. You can store multiple images ofthe same project with different changes and can still access each of the branches. Github provides actions like fork , clone to share and work with projects of other users on github.com. The most important feature of the github is that it can restore the image at any point of the commit. Commit is an action of approving changes that are applicable on both local and the remote repo. It means that whatever changes you've made on that project would be synced on your repo as well. According to me, this seems to the basic or fundamental working principle of the Github.
    


    

  
  # Git terms
     Before diving into the basic commands of the Git. We should first make ourselves,
     aware of few terms.


   - **init**: initiate a git into a local folder. This is the first step of working with git.
   - **repo**: repo is remote (at least for github) folder that holds your project that is watched by git for any commits or transaction.
   - **add** : add keyword adds the content to the github staging area.
   - **commit**: commit the changes made to the content that was previously in the staging area
   - **branch**: branch are the image of the project that will feature the original project but can also inherit changes made by the user.
   - **remote**: remote refers to an alias for an url for your repo
   - **origin**: origin is a default name for remote in github.
   - **pull**: pull a request to repo for making any changes.
   - **fork**: fork and clone are two different terms with slight differences in how they functions. Fork is a remote clone of the project on the user github account that
   - can be further edited and requested to be merged into your repo. Fork in simple term means to copy the project from one user account of git to the other account for their usage. But, the key characteristics is that it can be also requested for merging to the original repo after making changes.
   - **merge**: merge is a method to merge the changes to specific branches
   - **push**: push is to push all commits made to the project in the staging area to your repo using remote url.
   - **show** - shows the commits made before pushing into the branch.
   - **clone** - clone the repo to your local machine in a local folder similar to download.

 
  

  
  




