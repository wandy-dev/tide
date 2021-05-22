# tide
Tool for managing pods

  COMMANDS:

    ls:                                                   list pods
    rm <release>:                                         delete a release
    install <release_name> <service_name> <yaml_env>:     install a release
    upgrade <release_name> <service_name> <yaml_env>:     update yaml files for a release
    exec [<pod>] [<command>]:                             execute <command> on specified <pod> omit args to use fzf to select
    clean:                                                delete all persistent volume claims
    tail <pod>:                                           view logs of running pod
    show <pod>:                                           view pod metadata

  OPTIONS:
    -c: display helm/kubectl command for confirmation before execution
    -h: display this message

## Installation

Just download the script, make it executable, and put it somewhere in your PATH. I like to have a bin directory for scripts like this so running `cd; mkdir bin` and adding the following line to your .profile file `export PATH=~/bin:$PATH` should be all you need. You should now be able to run the tide command.

NOTE: If you want to help contribute, or get future updates, I recommend cloning this repo and then creating a symlink to your bin directory of choice. This will allow you to update the script by just pulling from github.

## Optional dependencies
[fzf](https://github.com/junegunn/fzf) This allows you to select a pod and a command to run. Rather than having to run `tide ls`, copy the pod name and running `tide exec <pod> <command>`. Now just run `tide exec` and select both the pod and the command to run using fzf. This requires adding commands to your tiderc file

## Configuration
Make a file at ~/.config/tide/tiderc

Add `COMMANDS=('bundle exec rails c' 'bash')` to the file.

Add any commands you want as a string separated by a space. Be sure to install fzf for the exec command to work.
