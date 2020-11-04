def artifactname = "sp-boot-app.jar"
def repoName = "sp-boot-app-repo"
def pipelineName = "devops_vk_pipeline"
def semanticVersion = "${env.BUILD_NUMBER}.0.0"
def packageName = "spboot-package_${env.BUILD_NUMBER}"
def version = "${env.BUILD_NUMBER}.0"
def buildNumber = "${env.BUILD_NUMBER}"
/////def orchToolId="1153dbd753f100107109ddeeff7b122e"  
//${env.BUILD_NUMBER}
pipeline {
	agent any
	tools {
		maven 'Maven'
	}
	stages {
		stage("checkout") {
		stages {
			stage('deploy to dev') {
				when {
					branch 'dev'
				}
				steps {
					echo "Building in UAT"
				}
			}
			stage('deploy to prod') {
				when {
					branch 'master'
				}
				steps {
					echo "Building in prod"
				}
			}
		}
	}

	stage("build") {
		stages {
			stage('deploy to dev') {
				when {
					branch 'dev'
				}
				steps {
					echo "Manual Building in UAT"
				}
			}
			stage('deploy to prod') {
				when {
					branch 'master'
				}
				steps {
					echo "Manual Building in prod"
				}
			}
		}
     }

	stage('unit-tests') {
		stages {
			stage('deploy to dev') {
				when {
					branch 'dev'
				}
				steps {
					echo "Manual Test in UAT"
				}
			}
			stage('deploy to prod') {
				when {
					branch 'master'
				}
				steps {
					echo "Manual Test in prod"
				 sleep 2
				
                                 writeFile file: 'aggregate-results-3.xml', text: '<?xml version="1.0" encoding="UTF-8"?><FinalStatus><TestDuration>60.0</TestDuration><Group label="http://localhost:8080/"><throughput value="104"><name>throughput</name><value>104</value></throughput><concurrency value="1"><name>concurrency</name><value>1</value></concurrency><succ value="104"><name>succ</name><value>104</value></succ><fail value="0"><name>fail</name><value>0</value></fail><avg_rt value="0.06435"><name>avg_rt</name><value>0.06435</value></avg_rt><stdev_rt value="0.03491"><name>stdev_rt</name><value>0.03491</value></stdev_rt><avg_lt value="0.01359"><name>avg_lt</name><value>0.01359</value></avg_lt><avg_ct value="0.00088"><name>avg_ct</name><value>0.00088</value></avg_ct><bytes value="156896844"><name>bytes</name><value>156896844</value></bytes><rc value="104" param="200"><name>rc/200</name><value>104</value></rc><perc value="0.04400" param="0.0"><name>perc/0.0</name><value>0.04400</value></perc><perc value="0.05800" param="50.0"><name>perc/50.0</name><value>0.05800</value></perc><perc value="0.08300" param="90.0"><name>perc/90.0</name><value>0.08300</value></perc><perc value="0.10300" param="95.0"><name>perc/95.0</name><value>0.10300</value></perc><perc value="0.12400" param="99.0"><name>perc/99.0</name><value>0.12400</value></perc><perc value="0.38100" param="99.9"><name>perc/99.9</name><value>0.38100</value></perc><perc value="0.38100" param="100.0"><name>perc/100.0</name><value>0.38100</value></perc></Group><Group label=""><throughput value="170"><name>throughput</name><value>170</value></throughput><concurrency value="2"><name>concurrency</name><value>2</value></concurrency><succ value="170"><name>succ</name><value>170</value></succ><fail value="0"><name>fail</name><value>0</value></fail><avg_rt value="0.20195"><name>avg_rt</name><value>0.20195</value></avg_rt><stdev_rt value="0.22618"><name>stdev_rt</name><value>0.22618</value></stdev_rt><avg_lt value="0.02789"><name>avg_lt</name><value>0.02789</value></avg_lt><avg_ct value="0.00098"><name>avg_ct</name><value>0.00098</value></avg_ct><bytes value="365675109"><name>bytes</name><value>365675109</value></bytes><rc value="170" param="200"><name>rc/200</name><value>170</value></rc><perc value="0.04400" param="0.0"><name>perc/0.0</name><value>0.04400</value></perc><perc value="0.07000" param="50.0"><name>perc/50.0</name><value>0.07000</value></perc><perc value="0.41700" param="90.0"><name>perc/90.0</name><value>0.41700</value></perc><perc value="0.48100" param="95.0"><name>perc/95.0</name><value>0.48100</value></perc><perc value="0.71200" param="99.0"><name>perc/99.0</name><value>0.71200</value></perc><perc value="2.12800" param="99.9"><name>perc/99.9</name><value>2.12800</value></perc><perc value="2.12800" param="100.0"><name>perc/100.0</name><value>2.12800</value></perc></Group><Group label="http://localhost:8080/"><throughput value="66"><name>throughput</name><value>66</value></throughput><concurrency value="1"><name>concurrency</name><value>1</value></concurrency><succ value="66"><name>succ</name><value>66</value></succ><fail value="0"><name>fail</name><value>0</value></fail><avg_rt value="0.41877"><name>avg_rt</name><value>0.41877</value></avg_rt><stdev_rt value="0.23020"><name>stdev_rt</name><value>0.23020</value></stdev_rt><avg_lt value="0.05044"><name>avg_lt</name><value>0.05044</value></avg_lt><avg_ct value="0.00112"><name>avg_ct</name><value>0.00112</value></avg_ct><bytes value="208778265"><name>bytes</name><value>208778265</value></bytes><rc value="66" param="200"><name>rc/200</name><value>66</value></rc><perc value="0.27700" param="0.0"><name>perc/0.0</name><value>0.27700</value></perc><perc value="0.36900" param="50.0"><name>perc/50.0</name><value>0.36900</value></perc><perc value="0.52600" param="90.0"><name>perc/90.0</name><value>0.52600</value></perc><perc value="0.63600" param="95.0"><name>perc/95.0</name><value>0.63600</value></perc><perc value="2.12800" param="99.0"><name>perc/99.0</name><value>2.12800</value></perc><perc value="2.12800" param="99.9"><name>perc/99.9</name><value>2.12800</value></perc><perc value="2.12800" param="100.0"><name>perc/100.0</name><value>2.12800</value></perc></Group></FinalStatus>'

				 sleep 2
				}
			}
		}
	}

	stage("deploy") {
		stages {
			stage('deploy to dev') {
				when {
					branch 'dev'
				}
				steps {
					echo "deploy in UAT"
				}
			}
			stage('deploy to prod') {
				when {
					branch 'master'
				}
				steps {
					echo "deploy in prod"
					snDevOpsChange()
				}
			}
		}
	}

}
}
