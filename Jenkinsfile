pipeline
{
agent any
stages
{
        
        stage ('scm checkout')
        
             {steps{gitgit 'https://github.com/nawnath24/maven-project.git'}}

        stage('validate')

             {steps{withMaven(globalMavenSettingsConfig: '', jdk: '', maven: '', mavenSettingsConfig: '', traceability: true) {
             sh 'mvm validate'
}}}

        stage('compile the code')
             {steps{withMaven(globalMavenSettingsConfig: '', jdk: '', maven: '', mavenSettingsConfig: '', traceability: true) {
             sh 'mvm compile'
}}}

        stage('package the code')
             {steps{withMaven(globalMavenSettingsConfig: '', jdk: '', maven: '', mavenSettingsConfig: '', traceability: true) {
             sh 'mvm package'
}}}

          
      
}
}