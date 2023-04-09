pipeline {

    // Agent, der definiert, wo die Pipeline ausgeführt wird
    agent {
        docker {
            image 'maven:3-alpine'  // Verwendet das Docker-Image 'maven:3-alpine' als Build-Umgebung
            args '-v /root/.m2:/root/.m2'  // Mountet das lokale Maven-Repository als Volume ins Docker-Image
        }
    }

    // Stages, die die einzelnen Schritte der Pipeline definieren
    stages {

        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'  // Führt das Maven Build aus und erstellt ein Jar-Paket
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'  // Führt die Tests aus
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'  // Sammelt Testergebnisse und zeigt sie in Jenkins an
                }
            }
        }

        stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh'  // Führt das Skript 'deliver.sh' aus, um das gebaute Artefakt auszuliefern
            }
        }
    }
}
