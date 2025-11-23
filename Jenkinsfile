pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                bat 'echo Build successful'
            }
        }

        stage('Deploy') {
            steps {
                bat '''
                    echo Deploying website...
                    
                    REM Clean existing files
                    del /Q C:\\inetpub\\wwwroot\\*
                    rmdir /S /Q C:\\inetpub\\wwwroot\\assets
                    
                    REM Copy new files
                    xcopy . C:\\inetpub\\wwwroot\\ /E /Y
                '''
            }
        }
    }
}
