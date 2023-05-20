pipeline {
  agent any

  stages {
    stage('Install Dependencies') {
      steps {
        // Install required dependencies (e.g., pip packages)
        sh 'pip install -r requirements.txt'
      }
    }

    stage('Run Tests') {
      steps {
        // Run Django tests
        sh 'python3 manage.py test'
      }
    }

    stage('Build') {
      steps {
        // Build any necessary static assets
        sh 'python3 manage.py collectstatic --noinput'
      }
    }

    // stage('Deploy') {
    //   steps {
    //     // Deploy your Django application (e.g., to a server or cloud platform)
    //     // Add the necessary commands or scripts to deploy your app
    //   }
    // }
  }
}
