node(){
    stage("clone code from scm"){
        git 'https://github.com/swathiraos/gol.git'
    }
    stage("build the code"){
        sh 'mvn package'
    }
}
