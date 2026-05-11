# GW4 Cytometry Data Science Workshop

Welcome to the official repository for the **GW4 Cytometry Data Science Workshop**, organised by the **Centre for Cytomics at the University of Exeter**.

This repository contains the launcher scripts and supporting information needed to run the workshop computing environment using **Docker** and **RStudio Server**.

The aim is to provide all participants with the same reproducible R environment, including the packages required for the practical sessions.

---

## Workshop environment

The workshop uses a Docker image containing RStudio Server and the required R packages.

Docker image:

```text
ghcr.io/exeter-cytomics/gw4_cytometry_data_science_workshop:gw-2026
```

When launched, the environment runs RStudio Server locally on your computer.

Open RStudio in your browser at:

```text
http://localhost:8787
```

Login details:

```text
Username: rstudio
Password: 1234
```

---

## What you need before the workshop

Before running the launcher, please install **Docker Desktop**

### Windows and macOS

Download Docker Desktop from:

[Download Docker Desktop](https://www.docker.com/products/docker-desktop/)

After installation, open Docker Desktop and make sure it is running before starting the workshop launcher.

### Linux

Install Docker Engine using the instructions appropriate for your Linux distribution.

---

## Running the workshop environment

The easiest way to start the workshop environment is to use one of the launcher scripts provided in the GitHub release.

Go to the **Releases** section of this repository and download the launcher for your operating system.

---

## Windows

Download:

```text
launch_gw4_workshop_windows.bat
```

Then double-click the file.

The launcher will:

1. Ask you to select a folder containing your data.
2. Download the workshop Docker image if needed.
3. Start RStudio Server.
4. Open RStudio in your browser.

Your selected folder will be available inside RStudio at:

```text
/home/rstudio/main
```

Keep the launcher window open while using RStudio.

When you are finished, press any key in the launcher window to stop and remove the running container.

---

## macOS and Linux

Download:

```text
launch_gw4_workshop_mac_linux.sh
```

Open a terminal in the folder where you downloaded the file and run:

```bash
chmod +x launch_gw4_workshop_mac_linux.sh
./launch_gw4_workshop_mac_linux.sh
```

The launcher will:

1. Ask you to select a folder containing your data.
2. Download the workshop Docker image if needed.
3. Start RStudio Server.
4. Open RStudio in your browser.

Your selected folder will be available inside RStudio at:

```text
/home/rstudio/main
```

Keep the terminal window open while using RStudio.

When you are finished, press Enter in the terminal to stop and remove the running container.

---

## First run

The first time you run the launcher, Docker will need to download the workshop image.

The image is large, so this may take several minutes depending on your internet connection.

Subsequent runs should be faster because Docker will already have the image stored locally.

---

## Accessing your files in RStudio

When the launcher asks you to select a folder, choose the folder containing your workshop data.

For example, on Windows this might be:

```text
C:\Users\YourName\Documents\GW4_workshop_data
```

On macOS or Linux this might be:

```text
/Users/YourName/Documents/GW4_workshop_data
```

Inside RStudio, this folder will appear as:

```text
/home/rstudio/main
```

Any files you save there from RStudio will also be saved back to the selected folder on your computer.

---

## Stopping the environment

To stop RStudio Server and clean up the running container:

- On Windows: press any key in the launcher window.
- On macOS/Linux: press Enter in the terminal window.

This stops and removes the running Docker container, but it does **not** remove:

- your data files,
- the downloaded Docker image,
- the launcher scripts.

---

## Troubleshooting

### Docker is not running

Make sure Docker Desktop is open and fully started before running the launcher.

### Port 8787 is already in use

RStudio Server uses port `8787`.

If another program is already using this port, the launcher may fail. Close the other program or restart Docker Desktop and try again.

### The browser does not open automatically

Open your browser manually and go to:

```text
http://localhost:8787
```

### Login information

Use:

```text
Username: rstudio
Password: 1234
```

### The image download is slow

The Docker image is large. The first download may take several minutes.

## Licence

This repository is licensed under the MIT License unless otherwise stated.

The Docker image may include third-party software and packages, each of which remains subject to its own licence.
