pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building..."'
                sh 'chmod +x project/src-Build.sh'
                sh 'project/Linux-Build.sh'
                archiveArtifacts artifacts: 'bin/Debug/*', fingerprint:true
            }
        }
    stage ('Test') {
        steps {
            sh 'echo "Running.."'
            sh 'chmod +x scripts/Linux-Run.sh'
            sh 'scripts/Linux-Run.sh'
            }
        }

    }
}
