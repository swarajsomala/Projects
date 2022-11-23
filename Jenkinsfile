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

        stage('Formatting Check') {
          steps {
            build(job: 'quality_formatting',
              parameters: []
            ) // build job
          } // steps
        } // Stage: EOL Check
        
    } // parallel
  } // stage: Quality Checks
 }
}
