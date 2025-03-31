whoosh Oktopus Installation Manual
---
Version: `5.26.0` - `2025-03-30` \
Author: [oktopus@freedom-manufaktur.com](mailto:oktopus@freedom-manufaktur.com) \
Link: [Documentation on GitHub](https://github.com/freedom-manufaktur/Oktopus/blob/main/Documentation/Oktopus%20Installation%20Manual.md)

Table of contents
---
<!--TOC-->
- [Installation](#installation)
  - [Installallation as Windows Service](#installallation-as-windows-service)
  - [Installation as Docker Container via Docker Compose](#installation-as-docker-container-via-docker-compose)
  - [Installation as Kubernetes Deployment via HELM Chart](#installation-as-kubernetes-deployment-via-helm-chart)
- [Upgrade](#upgrade)
  - [Upgrade a Windows Installation](#upgrade-a-windows-installation)
  - [Upgrade a Docker instance](#upgrade-a-docker-instance)
- [What's new?](#whats-new)
- [Need support?](#need-support)
<!--/TOC-->


# Installation
There are different kinds of installation. You may choose the one best suiting your needs.
- Windows Service \
   ✔ lightweight \
   ✔ easy to install, update and configure \
   ⚠ Windows only \
   ℹ .NET required (installed automatically)
- Docker Container via Docker Compose \
   ✔ containerized \
   ✔ cross platform \
   ⚠ Docker with [Docker Compose v2](https://docs.docker.com/compose/) required
- Kubernetes Deployment via [HELM Chart](https://helm.sh/) \
   ✔ containerized \
   ✔ scalable \
   ✔ cross platform \
   ⚠ Kubernetes installation required \
   ⚠ [HELM](https://helm.sh/docs/intro/install/) installation required \
   ⚠ Experience with Kubernetes and HELM Charts required


## Installallation as Windows Service

1. Download Installation from [whoosh Oktopus Download](https://freedommanufaktur.sharepoint.com/:f:/g/EjZZuA7_BmlNj52AO6_6lhwBjubo5u_hjfxS2FfauZYJHg?e=3zMX8j).

2. *(Optional, when offline*) Download and install the most recent [.NET 9.0 Runtimes](https://dotnet.microsoft.com/en-us/download/dotnet/9.0)
   1. ASP.NET Core Runtime x64 Installer
   2. .NET Desktop Runtime x64 Installer

3. Install `whoosh Oktopus Server Setup 5.26.0.exe`
   > Note: This will automatically install .NET 9.0 if necessary
   
   ![Windows Setup](<Images/Installation/Windows Installation.png>)

4. After the installation completes hit **Launch**. To open the *Server Settings* app.

5. Run the *Server Settings* app as admin.
   ![Server settings App without any environments](<Images/Installation/Server Settings empty.png>)

6. Add a new *Oktopus environment*.
   > An *environment* represents an isolated instance of the *Oktopus Server*. Each environments runs as a Windows service, has its own configuration and can be updated separately.
   
   ![Add new environment](<Images/Installation/Server Settings new environment.png>)
   ![View added environment](<Images/Installation/Server Settings environment.png>)

7. Click *Settings* and configure your instance according to your needs.
   
8. Start the environment.
   ![Running environments](<Images/Installation/Server Settings environment running.png>)

9.  (Optional, verify running) Open a browser and navigate to your Oktopus environment URL.\
    For example: https://oktopus.MyCompany.com or http://localhost:8080/
   
    > Note: Make sure to use the correct domain and port number based on **your** configuration.
   
    You should be greeted with the message\
    `whoosh Oktopus 5.26.0`

## Installation as Docker Container via Docker Compose

1.  Download Docker Image (`.tar`) from [whoosh Oktopus Download](https://freedommanufaktur.sharepoint.com/:f:/g/EjZZuA7_BmlNj52AO6_6lhwBjubo5u_hjfxS2FfauZYJHg?e=3zMX8j).

2.  [Contact us](mailto:oktopus@freedom-manufaktur.com) to help you with the installation.

## Installation as Kubernetes Deployment via HELM Chart

1.  Download Docker Image (`.tar`) from [whoosh Oktopus Download](https://freedommanufaktur.sharepoint.com/:f:/g/EjZZuA7_BmlNj52AO6_6lhwBjubo5u_hjfxS2FfauZYJHg?e=3zMX8j).

2.  [Contact us](mailto:oktopus@freedom-manufaktur.com) to help you with the installation.

# Upgrade

## Upgrade a Windows Installation
1.  (Optional, when Offline) Download and install the most recent [.NET 9.0 Runtimes](https://dotnet.microsoft.com/en-us/download/dotnet/9.0)
    1. ASP.NET Core Runtime x64 Installer
    2. .NET Desktop Runtime x64 Installer

2.  Install `whoosh Oktopus Server Setup vNext.exe`
    > Note: This will automatically install .NET 9.0 if necessary

3.  After the installation completes hit **Launch**. To open the *Server Settings* app.

4.  Run the *Server Settings* app as admin.
    ![Running environments](<Images/Installation/Server Settings environment running.png>)

5.  Click *Change version*, select the desired version number (defaults to the highest installed version) and confirm by clicking *Change version* again.
    ![Change environment version](<Images/Installation/Server Settings environment change version.png>)

6.  Your environment should now be updated.
    > Note: This includes changes the the Oktopus database.\
    Please read the `Oktopus changelog.md` to check for any breaking changes.

    > Note: The *whoosh Oktopus Workflow Studio* if often up- and downwards compatible with a different server version. We still **recommend** using *whoosh Oktopus Workflow Studio* with the same version as the server. Especially when there are breaking changes (see `Changelog.md`).

## Upgrade a Docker instance

1.  Follow the respective Docker installation instructions, but use the newer image tag.

# What's new?
This section lists **important** changes to the documentation and Docker files.
Please read this list when upgrading an existing installation.
> The full changelog can be found in the [whoosh Oktopus Download](https://freedommanufaktur.sharepoint.com/:f:/g/EjZZuA7_BmlNj52AO6_6lhwBjubo5u_hjfxS2FfauZYJHg?e=3zMX8j).

# Need support?
If you have any questions regarding the installation or configuration of *whoosh Oktopus*, contact us at [oktopus@freedom-manufaktur.com](mailto:oktopus@freedom-manufaktur.com) (freedom manufaktur).