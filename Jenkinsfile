node {
    stage( 'verificar repositorio' ){
        checkout scm
    }

    stage( 'Instalación de dependencias' ){
        bat 'npm installo' 
    }

    stage('Contruir Aplicacion'){
        bat( 'ng build' )
    }
}