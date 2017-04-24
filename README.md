# <img src="DiscordMusicBot/disc.png" width="42"> DiscordMusicBot
A Discord Bot for playing YouTube music.

# Installing
### Windows
1. [Add this Music Bot to your Discord Server](https://discordapp.com/oauth2/authorize?client_id=304226292545486849&scope=bot)
2. [Download this Music Bot](https://github.com/mrousavy/DiscordMusicBot/raw/master/Download/DiscordMusicBot.zip) and extract into **DiscordMusicBot/**
3. [Modify **config.json**](#configure)
4. [Install .NET Core](https://www.microsoft.com/net/download/core)
5. Optionally (Reinstall newer versions):
    * [Download FFmpeg](http://ffmpeg.zeranoe.com/builds/) and place into **DiscordMusicBot/** folder
    * [Download youtube-dl](https://rg3.github.io/youtube-dl/download.html) and place into **DiscordMusicBot/** folder
    * Download [Sodium](https://discord.foxbot.me/binaries/libsodium/) and/or [Opus](https://discord.foxbot.me/binaries/opus/) and place them into **DiscordMusicBot/** folder
6. Run
    * Commandline
    
    ```shell
    dotnet DiscordMusicBot.dll
    ```
    * Open Bat File
    `DiscordMusicBot.bat`

### Linux
1. [Add this Music Bot to your Discord Server](https://discordapp.com/oauth2/authorize?client_id=304226292545486849&scope=bot)
2. [Download this Music Bot](https://github.com/mrousavy/DiscordMusicBot/raw/master/Download/DiscordMusicBot.zip) and extract into **DiscordMusicBot/**
3. [Modify **config.json**](#configure)
4. [Install .NET Core](https://www.microsoft.com/net/download/linux)
5. Optionally (Reinstall newer versions):
    * [Download FFmpeg](https://ffmpeg.org/download.html#build-linux) and place into **DiscordMusicBot/** folder
    * [Download youtube-dl](https://rg3.github.io/youtube-dl/download.html): and place into **DiscordMusicBot/** folder
        ```shell
        sudo curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl

        sudo chmod a+rx /usr/local/bin/youtube-dl
        ```
     * Download [Sodium](https://download.libsodium.org/doc/installation/) and/or [Opus](http://opus-codec.org/downloads/) and place them into **DiscordMusicBot/** folder
6. Run
    * Bash (dotnet)
    
    ```shell
    dotnet DiscordMusicBot.dll
    ```
    * Bash (Script)
    
    ```shell
    sh DiscordMusicBot.sh
    ```
    

# Configure
### config.json
1. Create your app [here](https://discordapp.com/developers/applications/me)
2. Create **DiscordMusicBot/config.json** file
3. Paste this into **config.json** and set your values
    ```json
    {
    "ClientId": "[app Client ID]",
    "ClientSecret": "[app secret]",
    "BotName": "[app name]",
    "Token": "[app token]",
    "ServerName": "My Discord Server",
    "VoiceChannelName": "Lounge 1",
    "TextChannelName": "general"
    }
    ```
    
### users.txt
1. Enter names into users.txt (Name#Id, e.g.: Me#123)
2. Send DiscordMusicBot `!update` to update Permitted Client List, or restart

# Commands

`!add [url]`                            ...     Adds a single Song to Music-queue

`!addPlaylist [playlist-url]`           ...     Adds whole playlist to Music-queue

`!pause`                                ...     Pause the queue and current Song

`!play`                                 ...     Resume the queue and current Song

`!queue`                                ...     Prints all queued Songs & their User

`!clear`                                ...     Clear queue and current Song

`!setTimeout [timeoutInMilliseconds]`   ...     Timeout between being able to request songs

`!help`                                 ...     Prints available Commands and usage

`!come`                                 ...     Let Bot join your Channel

`!update`                               ...     Updates the Permitted Clients List from clients.txt

`!skip`                                 ...     Skips the current Song
