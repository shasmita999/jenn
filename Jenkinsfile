pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                // Get some code from a GitHub repository
                git url: 'https://github.com/shasmita999/jenn.git', branch: 'main'
                
            }
        }
        stage('Functional Test - HCL OneTest UI') {
            steps {
                echo("************************** Functional Test - HCL OneTest UI Start **************************")
                step([$class: 'RTWProductHelper', configfile: '', exportReportFileName: '', exportReportFolder: '', exportReportFormat: '', exportReportType: 'unified', exportReportUsage: false, exportstatreportlist: '', exportstats: '', exportstatsformat: '', exportstatshtml: '', imports: '', imsharedloc: 'C:\\Program Files\\IBM\\IBMIMShared', labels: '', name: 'GIT_Jenkins_UI', overwrite: 'true', project: 'Test_chrome', protocolinput: '', publish: '', publishfor: '', publishreports: '', quiet: 'false', results: '', suite: 'shhh.testsuite', swapdatasets: '', usercomments: '', varfile: '', vmargs: '', workspace: 'C:\\Users\\shasmita.swain\\HCL\\hclonetest\\new_test'])
                echo("************************** Functional Test - HCL OneTest UI End **************************")

            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}


