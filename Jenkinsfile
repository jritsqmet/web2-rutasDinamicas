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

    //BORRAR EL CONTENIDO DE LA CARPETA
    stage('Limpiar carpeta'){
        bat 'del /Q /S C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\angular-pipeline\\dist\\app-fire C:\\servidor\\angular'
    }

    stage('Mover al servidor'){
        bat 'xcopy C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\angular-pipeline\\dist\\app-fire C:\\servidor\\angular /E /I /Y'
    }
}