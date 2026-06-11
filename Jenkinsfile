
@Library('monitoring-shared-library') _

node('master') {

    def props = readProperties file: 'prod.properties'

    ansibleDeploy(

        REPO_URL: 'https://github.com/strangecodee/ansible-shared-library.git',

        BRANCH: props.BRANCH ?: 'main',

        INVENTORY: props.INVENTORY,

        PLAYBOOK: props.PLAYBOOK,

        ENVIRONMENT_NAME: props.ENVIRONMENT,

        SLACK_CHANNEL_NAME: props.SLACK_CHANNEL_NAME,

        ACTION_MESSAGE: props.ACTION_MESSAGE,

        KEEP_APPROVAL_STAGE: props.KEEP_APPROVAL_STAGE.toBoolean()
    )
}
