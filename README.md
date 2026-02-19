# Skript Workshop Docker

## 1. Vorraussetzungen

### 1.1 Windows

[Windows Terminal](https://apps.microsoft.com/detail/9n0dx20hk701?hl=de-DE&gl=DE)  
[PowerShell](https://learn.microsoft.com/de-de/powershell/scripting/install/install-powershell-on-windows?view=powershell-7.5#winget)  
[Git](https://git-scm.com/install/windows)  
[VSCode](https://code.visualstudio.com/download)

### 1.2 Mac

Mac Terminal  
[Git](https://git-scm.com/install/mac)  
[VSCode](https://code.visualstudio.com/download)

## 2. Installation

[Docker Desktop](https://docs.docker.com/get-started/get-docker/)

### 2.1 Windows (Admin Rechte für Installation benötigt)

[WSL installieren, aktivieren](https://docs.docker.com/desktop/setup/install/windows-install/#wsl-verification-and-setup) & [einrichten](https://learn.microsoft.com/en-us/windows/wsl/setup/environment)

Docker Desktop mit jeweiligem Installer installieren

### 2.2 Mac

Docker Desktop mit jeweiligem Installer installieren

## 3. Einführung Workshop

### 3.1 [Endergebnis](./result/)

Dieses git repository clonen

```sh
git clone https://github.com/SMehren/docker-workshop
```

Docker Desktop starten

```sh
cd ./result
docker compose up -d
```

Applikation startet auf [localhost](http://localhost)  
Datenbankverwaltung startet auf [db.localhost](http://db.localhost)

## 3.2 Images bauen - [Übung zu Dockerfiles](./exercise/README.md)

[Dokumentation](https://docs.docker.com/get-started/docker-concepts/building-images/)

## 4. [Workshop](https://docs.docker.com/get-started/workshop/)

Klonen des Ausgangsrepositories in einem Ordner eurer Wahl

```sh
git clone https://github.com/docker/getting-started-app.git ./docker-workshop-todo-app
```

### 4.1 [Containerisieren und Starten der Anwendung](https://docs.docker.com/get-started/workshop/02_our_app/)

### 4.2 [Anwendung Anpassen  & Interaktion mit Containern](https://docs.docker.com/get-started/workshop/03_updating_app/)

### 4.3 Github Repository für Projekt erstellen

.git Ordner löschen und ein neues privates git Repository in einem eigenen Account erstellen

### 4.4 Image auf GHCR hochladen (Optional)

[Dokumentation](https://docs.github.com/de/packages/working-with-a-github-packages-registry/working-with-the-container-registry)

[Personal Access Token auf Github erstellen](https://docs.github.com/de/packages/working-with-a-github-packages-registry/working-with-the-container-registry#authentifizierung-mit-personal-access-token-classic)

Mit Docker auf Github anmelden

```sh
export CR_PAT=<YOUR_TOKEN>
```

```sh
echo $CR_PAT | docker login ghcr.io -u <USERNAME> --password-stdin
```

Bauen & Hochladen unseres Images

```sh
docker build -t ghcr.io/<USERNAME>/docker-workshop-todo-app:latest .
docker push ghcr.io/<USERNAME>/docker-workshop-todo-app:latest
```

### 4.5 [Daten in Volumes persistieren](https://docs.docker.com/get-started/workshop/05_persisting_data/)

### 4.6 [Daten auf dem Filesystem des Hosts persistieren](https://docs.docker.com/get-started/workshop/06_bind_mounts/)

### 4.7 [Daten auf MySQL Container persistieren & Networking](https://docs.docker.com/get-started/workshop/07_multi_container/)

### 4.8 [Docker Compose](https://docs.docker.com/get-started/workshop/08_using_compose/)

### 4.8 [Image Best Practices](https://docs.docker.com/get-started/workshop/09_image_best/)

## 5 Abschluss- / Bonusaufgaben

Erstellt Docker Compose Projekte für ein- oder mehrere Themen eurer Wahl:

- Traefik, Ollama und Open WebUI als lokaler KI Chatbot
- Traefik, Ollama und n8n als lokale KI Automatisierung
- OpenClaw, Ollama für lokale autonome Agentenworkflows
