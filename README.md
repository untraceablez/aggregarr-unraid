![aggregarr-icon](agregarr.png)
# `aggregarr-unraid`

## Table of Contents

 * [What is Agregarr?](#what-is-agregarr)
 * [Self-Hosting](#self-hosting)
    * [Docker Run / Docker Compose](#docker-run--docker-compose)
    * [unRAID](#unraid)
        * [unRAID Requirements](#unraid-requirements)
        * [Install Agregarr from Community Applications](#installing-agregarr-from-community-applications)
        * [Configuring the Container](#configuring-the-container)
        * [Accessing Agregarr & First-Time Setup](#accessing-agregarr--first-time-setup)
* [Acknowledgements](#acknowledgements)


## What is Agregarr?

[**Agregarr**](https://github.com/agregarr/agregarr/) is an automated Plex collection management tool that regularly updates your Plex collections with content from multiple sources. It integrates with your existing media management tools to provide seamless collection automation.

### Features

* **Multiple Content Sources**: Trakt, IMDb, TMDB, Letterboxd, MDBList, FlixPatrol, AniList, and MyAnimeList
* **Media Management Integration**: Works with Radarr and Sonarr for automated media acquisition
* **Request Integration**: Connects with Overseerr for request management
* **Statistics**: Integrates with Tautulli for viewing statistics
* **Coming Soon Feature**: Show upcoming releases (requires media volume mounts)
* **Automated Collection Updates**: Keep your Plex collections fresh and up-to-date

## Self-Hosting

### Docker Run / Docker Compose

This is a container template for hosting Agregarr on [unRAID](https://unraid.net/). If you are not using unRAID, you can use the official Docker image directly from [agregarr/agregarr](https://hub.docker.com/r/agregarr/agregarr/). For detailed setup instructions, see the [official Agregarr repository](https://github.com/agregarr/agregarr/).

### unRAID

This template is designed specifically for unRAID users. You should be able to find this template in Community Applications by searching for `agregarr`.

#### unRAID Requirements

* **Plex Media Server**: Agregarr manages Plex collections
* **Radarr and/or Sonarr** (recommended): For automated media management
* **Overseerr** (optional): For request integration
* **Tautulli** (optional): For statistics integration

#### Installing Agregarr from Community Applications

To install Agregarr from Community Applications, simply navigate to Community Apps and search for `agregarr`.

#### Configuring the Container

When you get to the container configuration page in unRAID:

1. **Port**: Default is 7171, change if needed
2. **Config Directory**: Set to `/mnt/user/appdata/aggregarr` (or your preferred location)
3. **Movies Directory** (Optional): If you want to use the Coming Soon feature, set this to match your Radarr movie path (e.g., `/mnt/user/media/movies`)
4. **TV Shows Directory** (Optional): If you want to use the Coming Soon feature, set this to match your Sonarr TV path (e.g., `/mnt/user/media/tv`)
5. **Timezone**: Set to your local timezone (e.g., `America/New_York`)

**Important**: For the Coming Soon feature to work properly, the media paths must exactly match the paths used in your Radarr and Sonarr containers.

#### Accessing Agregarr & First-Time Setup

After starting the container, navigate to `http://SERVERIP:7171` (or your configured port) to access the Agregarr web interface.

From there, you can:
1. Configure your Plex server connection
2. Set up Radarr and Sonarr integrations
3. Connect your content sources (Trakt, IMDb, etc.)
4. Configure Overseerr and Tautulli if desired
5. Start creating and managing automated collections


## Acknowledgements

* Thanks to the [Agregarr team](https://github.com/agregarr/agregarr/) for creating this excellent tool
* Thanks to the unRAID community for their continued support and contributions
