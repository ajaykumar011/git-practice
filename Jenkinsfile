// Powered by Infostretch 

timestamps {

node () {

	stage ('ssh-publish - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'git-crendetials', url: 'https://github.com/ajaykumar011/git-practice.git']]]) 
	}
	stage ('ssh-publish - Build') {
 	
// Unable to convert a build step referring to "jenkins.plugins.publish__over__ssh.BapSshPreBuildWrapper". Please verify and convert manually if required.
// Unable to convert a build step referring to "jenkins.plugins.publish__over__ssh.BapSshPostBuildWrapper". Please verify and convert manually if required.
// Unable to convert a build step referring to "hudson.plugins.timestamper.TimestamperBuildWrapper". Please verify and convert manually if required.		// Shell build step
sh """ 
echo "Build is in progress" 
 """
		archiveArtifacts allowEmptyArchive: false, artifacts: '*', caseSensitive: true, defaultExcludes: true, fingerprint: false, onlyIfSuccessful: false 
	}
}
}