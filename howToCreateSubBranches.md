# How to create sub-branches

For this example, there are two branches: `master` and `dev`.

Let’s say you want to create a feature branch off of dev. Let’s see what that would look like: 

1. Checkout the branch you want to branch from (`dev` in this case):
    ```
    git checkout dev
    ```
1. Create the new sub-branch (locally), we'll call it devSubBranch:
    ```
    git branch -b devSubBranch dev
    ```
    - You'll notice we included `dev`, you don't always have to do this if the HEAD is currently pointing to it, but doing so guarentees the branch being created correctly.

1. Push the branch to the remote:
    ```
    git push origin devSubBranch
    ```
1. Make and push your inital commmit:
    ```
    git add .
    git commit -m "initial commit"
    ```
1. Before you `git push`, make sure to set your upstream branch:
    ```
    git push --set upstream origin devSubBranch
    ```
1. Check your Github repository to ensure your push was successful
1. Happy coding!

