# This is an empty go lang project.

This is meant for quick development in VS Code using the dev container extension.

To get started: 
1. Open the project in a dev container. 
    * VS Code will usually prompt you to open the dev container when you open the directory.
    * You can always use ctrl+shift+p and type in:
    ```
    Dev Container: Rebuild and Reopen in Container.
    ```
2. Start a Go Project.
    * In the container terminal type: 
    ```
    go mod init *project-name
    ```
3. Start a fresh version control repository.
    * In the container terminal type:
    ```
    rm -rf .git && git init
    ```
4. Start developing.