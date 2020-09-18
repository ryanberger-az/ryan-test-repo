pipeline {
    agent {
      node {
        label 'win16-ssh'
      }
    }
    stages {
      stage('Prepare Windows Node') {
        steps { 
          powershell """
          Write-Output \'Jenkins build URL is ${BUILD_URL}\'
          Write-Output \'Jenkins URL is ${JENKINS_URL}\' 
          Write-Output \'Jenkins Branch is ${BRANCH_NAME}\'
          Write-Output \'Jenkins Workspace is set to: ${WORKSPACE}\'
          Write-Output \'Blue ocean build link ${JENKINS_URL}blue/organizations/jenkins/${CI_REPO_NAME}/detail/${BRANCH_NAME}/${BUILD_ID}\'
          powershell 'ls'
        }
      }
    }
}