node(){
    stage("clone code from scm"){
        git 'https://github.com/swathiraos/gol.git'
    }
    stage("build the code"){
        sh 'mvn package'
    }
    stage("postbuild"){
	    archiveArtifacts 'gameoflife-web/target/*.war'
            junit 'gameoflife-web/target/surefire-reports/*.xml'
	}
    stage("triggers") {
        pollSCM '*/1 * * * *'
    }
}
