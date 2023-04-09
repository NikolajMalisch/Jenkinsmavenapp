# Jenkinsmavenapp
Jenkins Pipeline mit Maven, Docker und JUnit
Dieses Repository enthält eine Beispiel-Jenkins-Pipeline, die eine Maven-Anwendung baut, testet und bereitstellt, sowie JUnit-Testergebnisse archiviert. 
Die Pipeline läuft in einer Docker-Umgebung und verwendet das Maven-Image von Docker Hub.

Voraussetzungen
Eine Jenkins-Installation mit installiertem Docker-Plugin
Ein Docker-Image mit Maven
Eine Anwendung, die mit Maven gebaut werden kann
Pipeline-Schritte
Die Pipeline besteht aus den folgenden Schritten:

Build: Baut die Maven-Anwendung, die sich im Repository befindet, unter Verwendung des Docker-Images mit Maven.
Test: Führt die JUnit-Tests der Anwendung aus und archiviert die Testergebnisse.
Deliver: Bereitet die Anwendung für die Bereitstellung vor und führt den Bereitstellungsskript deliver.sh aus.
Verwendung
Laden Sie diese Jenkins-Pipeline in Ihre Jenkins-Instanz hoch.
Passen Sie die Pipeline an Ihre Anwendung an, indem Sie den Namen der Anwendung und den Pfad zu Ihrem Bereitstellungsskript aktualisieren.
Starten Sie die Pipeline und überwachen Sie die Ausgabe, um sicherzustellen, dass die Schritte erfolgreich ausgeführt werden.
