# v35 automerge with post-update command failure

How to run:

```sh
export RENOVATE_ALLOW_POST_UPGRADE_COMMAND_TEMPLATING=true
export RENOVATE_ALLOWED_POST_UPGRADE_COMMANDS="bump"
export LOG_LEVEL=debug
renovate thejan2009/renovate-automerge
# wait 30 seconds
renovate thejan2009/renovate-automerge
```

Observe the following logs the second time around:

```text
DEBUG: manager.getUpdatedPackageFiles() reuseExistingBranch=true (repository=thejan2009/renovate-automerge, branch=renovate/amazon-aws-cli-2.x)
DEBUG: Found a multistage build stage name: deployable (repository=thejan2009/renovate-automerge, branch=renovate/amazon-aws-cli-2.x)
DEBUG: Rebasing branch after deps list has changed (repository=thejan2009/renovate-automerge, packageFile=Dockerfile, branch=renovate/amazon-aws-cli-2.x)
       "depName": "amazon/aws-cli"
```

Dates below are added automatically:
2023-03-13-124958
2023-03-17-133129
