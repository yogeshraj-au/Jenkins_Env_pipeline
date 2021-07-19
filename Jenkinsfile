def mvn(def args) {
    def mvnHome = tool 'M3'
    def javaHome = tool 'JDK8'

    withEnv(["JAVA_HOME=${javaHome}", "PATH+MAVEN=${mvnHome}/bin:${env.JAVA_HOME}/bin"]) {
        sh "${mvnHome}/bin/mvn ${args} --batch-mode -V -U -e -Dsurefire.useFile=false"
        sh "java --version"
        sh "mvn --version"
    }
}
