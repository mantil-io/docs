# Mantil CLI Commands

Mantil command line interface commands.

### Singup process related commands

| command | description |
| --------| ----------- | 
| [user register](mantil_user_register.md) | Initiate Mantil registration |
| [user activate](mantil_user_activate.md) | Finalize Mantil registration |


### AWS account related commands

| command | description |
| --------| ----------- | 
| [aws install](mantil_aws_install.md) | Install Mantil into AWS account |
| [aws uninstall](mantil_aws_uninstall.md) | Uninstall Mantil from AWS account |
| [aws nodes](mantil_aws_nodes.md) | List Mantil aws nodes |


### Stage related commands

| command | description |
| --------| ----------- | 
| [stage new](mantil_stage_new.md) | Create a new stage |
| [stage destroy](mantil_stage_destroy.md) | Destroy a stage |
| [stage list](mantil_stage_list.md) | List stages in project |
| [stage use](mantil_stage_use.md) | Set default project stage |

### Project related commands

| command | description |
| --------| ----------- | 
| [new](mantil_new.md) | Create a new Mantil project |
| [deploy](mantil_deploy.md) | Deploy updates to stage |
| [invoke](mantil_invoke.md) | Invoke api method for current project and stage |
| [watch](mantil_watch.md) | Watch for file changes and automatically deploy them |
| [test](mantil_test.md) | Run project integration tests |
| [logs](mantil_logs.md) | Fetch logs for a specific API |
| [env](mantil_env.md) | Export project environment variables |
| [generate api](mantil_generate_api.md) | Generate Go code for a new API |
