# Mantil CLI Commands

Mantil command line interface commands.

### Singup process related commands

| command | description |
| --------| ----------- | 
| [mantil user register](mantil_user_register.md) | Initiates Mantil registration |
| [mantil user activate](mantil_user_activate.md) | Finalizes Mantil registration |


### AWS account related commands

| command | description |
| --------| ----------- | 
| [mantil aws install](mantil_aws_install.md) |  Install Mantil into AWS account |
| [mantil aws uninstall](mantil_aws_uninstall.md) |  Uninstall Mantil from AWS account |
| [mantil aws nodes](mantil_aws_nodes.md) | List Mantil aws nodes |


### Stage related commands

| command | description |
| --------| ----------- | 
| [mantil stage new](mantil_stage_new.md) | Create a new stage |
| [mantil stage destroy](mantil_stage_destroy.md) | Destroy a stage |
| [mantil stage list](mantil_stage_list.md) | List stages in project |
| [mantil stage use](mantil_stage_use.md) | Set default project stage |

### Project related commands

| command | description |
| --------| ----------- | 
| [mantil new](mantil_new.md) | Initializes a new Mantil project |
| [mantil deploy](mantil_deploy.md) | Deploys updates to stage |
| [mantil invoke](mantil_invoke.md) | Invoke api method for current project and stage |
| [mantil watch](mantil_watch.md) | Watch for file changes and automatically deploy them |
| [mantil test](mantil_test.md) | Run project integration tests |
| [mantil logs](mantil_logs.md) | Fetch logs for a specific function/api |
| [mantil env](mantil_env.md) | Export project environment variables |
| [mantil generate api](mantil_generate_api.md) | Generate Go code for a new API |
