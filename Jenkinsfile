node {
    stage( 'verificar repositorio' ){
        checkout scm
    }

    stage( 'Instalación de dependencias' ){
        bat 'npm install' 
    }

    stage('Contruir Aplicacion'){
        bat 'npm run ng build' 
    }

    stage('Mover al servidor'){
        bat 'xcopy C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\angular-pipeline\\dist\\app-fire C:\\servidor\\angular /E'
    }
}