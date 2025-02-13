pipeline{
    agent any
    stages{
        stage('scm checkout'){
            steps{git 'https://github.com/nawnath24/maven-project.git'}
        }
        stage('mvn validate'){
            steps{
                withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true) {
                    sh 'mvn validate'
                }
    

            }
        }
        stage('mvn compile'){
            steps{
                withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true) {
                    sh 'mvn compile'
                }
            }
        }
        stage('mvn package'){
            steps{
                withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true) {
                    sh 'mvn package'
                }
            }
        }
    }
}