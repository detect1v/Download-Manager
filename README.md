# Download-Manager

A Java desktop application for managing file downloads with pause/resume support, download speed control, persistent statistics, browser integration, and peer-to-peer file sharing.

## Features

* **Download Management** — Start, pause, resume, and cancel downloads.
* **Concurrent Downloads** — Run multiple downloads simultaneously.
* **Progress Tracking** — Monitor download progress, file size, and transfer speed.
* **Speed Limiting** — Configure maximum download speed and distribute bandwidth between active downloads.
* **Persistent Storage** — Store download information and statistics in an SQLite database.
* **Statistics** — Track download count, downloaded size, and download duration.
* **P2P File Sharing** — Share and download files between connected peers.
* **Browser Integration** — Send download links directly from Chrome and Firefox extensions.
* **Desktop Notifications** — Receive notifications about download status changes.

## Architecture

The application is organized into several layers:

* **GUI** — JavaFX-based user interface.
* **Service** — Download management, statistics, and speed distribution.
* **Repository** — Database access and persistence.
* **Model** — Application data and entities.
* **Utilities** — Commands, observers, iterators, composites, and P2P networking.

## Technologies

* **Java 17**
* **JavaFX**
* **SQLite**
* **Maven**

## Design Patterns

The project uses several design patterns:

* **Template Method**
* **Command**
* **Observer**
* **Composite**
* **Iterator**
* **Repository**

## Browser Integration

The project includes extensions for Google Chrome and Mozilla Firefox.

Downloads can be added to the application through a local HTTP endpoint:

```text
POST http://localhost:8080/api/download/add?url=<URL>
```

## Configuration

Application settings are stored in `config.properties` and include:

* Download directory
* Maximum download speed
* P2P shared directory
* P2P port
* Central server address and port

## How to Run

### Requirements

* Java 17+
* Maven

### Start the application

```bash
git clone https://github.com/detect1v/Download-Manager.git
cd Download-Manager/DownloadManager
mvn clean javafx:run
```

## Project Structure

```text
DownloadManager/
├── src/
│   ├── main/
│   │   ├── java/
│   │   └── resources/
│   └── test/
├── pom.xml
└── README.md
```
