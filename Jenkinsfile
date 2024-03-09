pipeline {
    agent any 
    
    // tools {
    //     maven "maven3.8"
    // }
    
    parameters { choice(name: 'BRANCH', choices: ['main', 'dev'], description: 'Environment') }
    
     
    environment {
        GIT_REPOSITORY = "https://github.com/tranvannhan1911/sample-github-action.git"
        // DOCKER_REPOSITORY = "tranvannhan1911/hiitfigure"
        // DOCKERHUB_CREDENTIAL = credentials('dockerhub')
    }
    
    stages {
        stage("Checkout"){
            steps {
                script{
                    def branchName = env.BRANCH_NAME
                    echo "Branch name is: ${branchName}"
                    // checkout scmGit(branches: [[name: '**']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/tranvannhan1911/sample-github-action']])
                    // checkout([$class: 'GitSCM', 
                    //     branches: [[name: BRANCH]],
                    //     extensions: [[$class: 'CleanCheckout']], // clean workspace after checkout
                    //     userRemoteConfigs: [[url: GIT_REPOSITORY]]])
                }
            }
        }
    }
}
