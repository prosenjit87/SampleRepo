pipeline {
  agent any
  stages {
    stage('Download') {
      parallel {
        stage('Download Hybris Package') {
          steps {
            echo 'Hybris Package download'
          }
        }
        stage('Download Project CodeBase') {
          steps {
            echo 'Project code base to be downloaded '
          }
        }
      }
    }
    stage('Merge Process') {
      steps {
        echo 'Merge project code inside Hybris package'
      }
    }
    stage('Compilation') {
      steps {
        echo 'Code compilation'
        echo 'some'
      }
    }
    stage('Junit') {
      steps {
        echo 'Run Junit'
      }
    }
    stage('Static Code Scan') {
      parallel {
        stage('Sonar') {
          steps {
            echo 'Run Sonar'
          }
        }
        stage('Fortify') {
          steps {
            echo 'Run Fortify'
          }
        }
        stage('EsLint') {
          steps {
            echo 'Run EsLint'
          }
        }
        stage('CheckMarx') {
          steps {
            echo 'Run Checkmarx'
          }
        }
        stage('Vulas') {
          steps {
            echo 'Run Vulas'
          }
        }
      }
    }
	stage('IPScan and PPMS') {
      parallel {
        stage('PPMS') {
          steps {
            echo 'Run PPMS'
          }
        }
        stage('Whitesource') {
          steps {
            echo 'Run whitesource'
          }
        }
      }
    }
    stage('IAT Automation') {
      steps {
        echo 'Run Automation'
      }
    }
	stage('Performance') {
      steps {
        echo 'Run performance'
      }
    }
    stage('Promote') {
      steps {
        echo 'Promote the code'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy code to server'
      }
    }
  }
}
