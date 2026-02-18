# Skript Workshop Docker

## 1. Vorraussetzungen

### 1.1 Windows

[Windows Terminal](https://apps.microsoft.com/detail/9n0dx20hk701?hl=de-DE&gl=DE)  
[PowerShell](https://learn.microsoft.com/de-de/powershell/scripting/install/install-powershell-on-windows?view=powershell-7.5#winget)  
[Git](https://git-scm.com/install/windows)

### 1.2 Mac

Mac Terminal  
[Git](https://git-scm.com/install/mac)

## 2. Installation

[Docker Desktop](https://docs.docker.com/get-started/get-docker/)

### 2.1 Windows (Admin Rechte für Installation benötigt)

[WSL installieren, aktivieren](https://docs.docker.com/desktop/setup/install/windows-install/#wsl-verification-and-setup) & [einrichten](https://learn.microsoft.com/en-us/windows/wsl/setup/environment)

Docker Desktop mit jeweiligem Installer installieren

### 2.2 Mac

Docker Desktop mit jeweiligem Installer installieren

## 3. Einführung Workshop

### 3.1 [Endergebnis](./result/)

Docker Desktop starten

```sh
cd ./aufgabe-1
docker compose up -d
```

Applikation startet auf [localhost](http://localhost)  
Datenbankverwaltung startet auf [db.localhost](http://db.localhost)

## 3.2 Images bauen - [Übung zu Dockerfiles](./exercise-1/README.md)

## 4. Workshop

