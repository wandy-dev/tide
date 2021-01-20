# tide
Tool for managing pods

  COMMANDS:

    ls:                                                   list pods
    rm <release>:                                         delete a release
    install <release_name> <service_name> <yaml_env>:     install a release
    upgrade <release_name> <service_name> <yaml_env>:     update yaml files for a release
    exec <pod> <command>:                                 execute <command> on specified <pod>
    clean:                                                delete all persistent volume claims
    tail <pod>:                                           view logs of running pod
    show <pod>:                                           view pod metadata

  OPTIONS:
    -c: display helm/kubectl command for confirmation before execution
    -h: display this message

## Installation

Just download the script, make it executable, and put it somewhere in your PATH. I like to have a bin directory for scripts like this so running `cd; mkdir bin` and adding the following line to your .profile file `export PATH=~/bin:$PATH` should be all you need. You should now be able to run the tide command.

NOTE: If you want to help contribute, or get future updates, I reccommend cloning this repo and then creating a symlink to your bin directory of choice. This will allow you to update the script by just pulling from github.
