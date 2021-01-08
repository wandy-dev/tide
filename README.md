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
