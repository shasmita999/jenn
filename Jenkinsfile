pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                // Get some code from a GitHub repository
                git url: 'https://github.com/shasmita999/Jenkins_GIT.git', branch: 'main'
                
            }
        }
        stage('Functional Test - HCL OneTest UI') {
            steps {
                echo("************************** Functional Test - HCL OneTest UI Start **************************")
                step([$class: 'RTWProductHelper', configfile: '', exportReportFileName: '', exportReportFolder: 'C:\\RE', exportReportFormat: '', exportReportType: 'unified', exportReportUsage: false, exportstatreportlist: '', exportstats: '', exportstatsformat: '', exportstatshtml: '', imports: '', imsharedloc: 'C:\\Program Files\\IBM\\IBMIMShared', labels: '', name: 'GIT_UI', overwrite: 'true', project: 'WebUIProj', protocolinput: '', publish: '', publishfor: '', publishreports: '', quiet: 'false', results: '', suite: 'checkExistence.testsuite', swapdatasets: '', usercomments: '', varfile: '', vmargs: '', workspace: 'C:\\Users\\shasmita.swain\\HCL\\hclonetest\\new10_5_1\\WebUIProj'])
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


