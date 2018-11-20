pipeline {
    agent any
    stages {
        stage('Checkout Repositories') {
            steps {
              dir('ckan') {
                checkout resolveScm(source: [$class: 'GitSCMSource', credentialsId: '', id: '_', remote: 'https://github.com/ckan/ckan.git', traits: [[$class: 'BranchDiscoveryTrait'], [$class: 'CloneOptionTrait', extension: [depth: 5, noTags: true, reference: '', shallow: true]], [$class: 'LocalBranchTrait']]], targets: [BRANCH_NAME,'master'])
              }
              dir('ckan2') {
                checkout resolveScm(source: [$class: 'GitSCMSource', credentialsId: '', id: '_', remote: 'https://github.com/ckan/ckan.git', traits: [[$class: 'BranchDiscoveryTrait'], [$class: 'CloneOptionTrait', extension: [depth: 5, noTags: true, reference: '', shallow: true]], [$class: 'LocalBranchTrait']]], targets: [BRANCH_NAME,'master'])
              }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
