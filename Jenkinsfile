pipeline { 
    agent any  
    stages { 
        stage('Build') { 
            steps { 
               echo 'This is a minimal pipeline.' 
            }
        }
        stage('CPP Check') {
            steps {
                // First, reset the error counters to match master.
                build( job: 'quality_cppcheck',
                    propagate: false,
                    parameters: [
                        string(name: 'BRANCH_YL', value: 'master'),
                        string(name: 'BRANCH_AA', value: 'master'),
                        string(name: 'BRANCH_SA', value: 'master'),
                        string(name: 'MERGE_FOR_YOCTO_LAYERS', value: 'master'),
                        string(name: 'MERGE_FOR_ARA_API', value: 'master'),
                        string(name: 'MERGE_FOR_SAMPLE_APPS', value: 'master')
                    ]
                ) // build job
            } // steps
        } // Stage: cpp check
    }
}
