pipeline {
  agent {
    label 'jenkins-slave-ansible'
  }

  stages {

    // Checkout source code
    // This is required as Pipeline code is originally checkedout to
    // Jenkins Master but this will also pull this same code to this slave
    stage('Git Checkout') {
      steps {
        // Turn off Git's SSL cert check, uncomment if needed
        // sh 'git config --global http.sslVerify false'
        git url: "https://github.com/bparry02/ansible-ci-test.git", branch: "master"
      }
    }

    stage('Build'){
      steps {
        sh "ansible --version"
      }
    }
  }
}
