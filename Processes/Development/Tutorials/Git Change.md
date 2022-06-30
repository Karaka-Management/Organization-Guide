# Git Change

## Basis

* Git is installed
* The user has access to the code base
* The tutorial uses the `Karaka.git` repository URL. You may want to replace this with a different repository.

## Tutorial

Create a new clone if you have not done so already in a previous tutorial.

```sh
git clone --recursive -j8 https://github.com/Karaka-Management/Karaka.git
```

You may be required to enter your username and password/authentication key from github.

If you already cloned the repository in the past you don't need to clone it again but "update" it with a pull.

```sh
git pull --recurse-submodules
```

Now you need to create a new branch for the changes you would like to do. Please follow the branch guidelines.

```sh
git checkout -b NEW_BRANCH_NAME
```

Sometimes you would like to work on multiple unrelated changes. In such a situation you should have created different branches for these changes. You can switch between branches with a checkout.

```sh
git checkout EXISTING_BRANCH_NAME
```

> It is recommended to run the above mentioned git pull command after switching a branch to get the newest version of the branch. 

After making your changes you can save them with a comment/message which describes your changes.

```sh
git commit -m "YOUR MESSAGE"
```

or with

```sh
git commit
```

This opens a window where you can write a longer text message.

Often it is recommended to do commits whenever you made a change which accomplishes one sub task. This way you can break down your changes in smaller changes which makes it easier for people to check and understand the code changes.

After everything is done you push the changes online for review.

```sh
git push --recurse-submodules
```

You may be required to once again enter your username and password/authentication key from github.

This creates a pull request which is a request to put your code changes into the online code base and eventually merge it with the main version of the code.

Please note that your code changes may not get accepted if they don't uphold the coding standards mentioned in the developer guide or if the code changes don't fit the goal of the code base.



2021-01-01 - Version 1.0