# vscode-container-dotfiles

This is an example dotfiles repositiory to be used with [Visual Studio Code - Remote Containers](https://code.visualstudio.com/docs/remote/containers#_personalizing-with-dotfile-repositories) functionality.

# Example usage

Update your user `settings.json` with the following:

```
    "remote.containers.dotfiles.repository": "uselessinfo/vscode-container-dotfiles",
    "remote.containers.dotfiles.installCommand": "/root/dotfiles/install.sh",
    "remote.containers.dotfiles.targetPath": "/root/dotfiles"
```

If it is working, you should see the following in the logs when you run `Remote-Containers: Show Log`:

```
[53391 ms] Start: Run in container: # Clone & install dotfiles
[54042 ms] 
[54043 ms] Cloning into '/root/dotfiles'...
```
