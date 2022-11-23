pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'This is a minimal pipeline.'
      }
    }
    stage('Quality Checks') {
      parallel {
        stage('CPP Check') {
          steps {
            build(job: 'quality_cppcheck',
              propagate: false,
              parameters: []
            ) // build job
          } // steps
        } // Stage: cpp check

        stage('EOL Check') {
          steps {
            build(job: 'quality_eol-disclaimer',
              parameters: []
            ) // build job
          } // steps
        } // Stage: EOL Check

        stage('Formatting Checks') {
          steps {
            build(job: quality_formatting]
          ) // build job
        } // steps
      } // Stage: Formatting Checks
    } // parallel
  } // stage: Quality Checks
 }
}
