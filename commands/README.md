# Mantil CLI Commands

Mantil command line interface commands.

### Singup process related commands

| command | description |
| --------| ----------- | 
| [activate](mantil_activate.md) | Activates Mantil |


### AWS account related commands

| command | description |
| --------| ----------- | 
| [aws install](mantil_aws_install.md) | Installs Mantil into AWS account |
| [aws uninstall](mantil_aws_uninstall.md) | Uninstalls Mantil from AWS account |
| [aws nodes](mantil_aws_nodes.md) | List Mantil AWS nodes |
| [aws resources](mantil_aws_resources.md) | Shows AWS resources created by Mantil |


### Stage related commands

| command | description |
| --------| ----------- | 
| [stage new](mantil_stage_new.md) | Creates a new stage |
| [stage destroy](mantil_stage_destroy.md) | Destroys a stage |
| [stage list](mantil_stage_list.md) | Lists stages in project |
| [stage use](mantil_stage_use.md) | Sets default project stage |

### Project related commands

| command | description |
| --------| ----------- | 
| [new](mantil_new.md) | Creates a new Mantil project |
| [deploy](mantil_deploy.md) | Deploys project updates to a stage |
| [invoke](mantil_invoke.md) | Invokes API method on the project stage |
| [watch](mantil_watch.md) | Watches for file changes and automatically deploy them |
| [test](mantil_test.md) | Runs project tests |
| [logs](mantil_logs.md) | Fetches logs for a specific API |
| [env](mantil_env.md) | Exports project environment variables |
| [generate api](mantil_generate_api.md) | Generates Go code for a new API |
