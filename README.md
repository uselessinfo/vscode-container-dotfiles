# vscode-container-dotfiles

This is an example dotfiles repositiory to be used with [Visual Studio Code - Remote Containers](https://code.visualstudio.com/docs/remote/containers#_personalizing-with-dotfile-repositories) functionality.

This is just an example. I would recommend creating yours as a private repo so you don't have to worry about what you put in it. VSCode will be able to access your private repositories through HTTPS or SSH without any issues.

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

# Gotchas

Make sure your `install.sh` script is executable, or the install process will fail.

There are two sets of settings `remote.containers.dotfiles...` and `dotfiles...`. I don't know how they differ, but make sure to pick the `remote.containers.dotfiles` settings, just in case. 

The example above is assuming your container is running with the root user. If not, those example settings will need to be tweaked.
