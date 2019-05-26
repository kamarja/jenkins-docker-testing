job('DSLNode') {
    scm {
        git('git@github.com:kamarja/jenkins-docker-testing.git') { node ->
            node / gitConfigName('DSL User')
            node / gitConfigEmail('kamarja@gmail.com')
        }
    }
    triggers {
        scm('H/5 * * * *')
    }
    wrappers {
        nodejs('NodeJS 10.10.0')
    }
    steps {
         shell("npm install")
        // dockerBuildAndPublish {
        //     repositoryName('kamarja/docker-example')
        //     tag('${GIT_REVISION,length=9}')
        //     registoryCredentials('07de667e-2367-40d0-a0b9-bc8cbf6119b3')
        //     forcePull(false)
        //     forceTag(false)
        //     createFingerprints(false)
        //     skipDecorate()
        // }
    }
}