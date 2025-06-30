# Dailymotion Pro

**Contributors:** Dailymotion Development Team  
**Tags:** video player, dailymotion, video, embed, media  
**Requires at least:** WordPress 6.0  
**Tested up to:** WordPress 6.8.1  
**Stable tag:** 6.0  
**Requires PHP:** 8.0  
**License:** GPLv2 or later  
[GPL License](https://www.gnu.org/licenses/gpl-2.0.html)

The official Dailymotion Pro WordPress plugin that seamlessly integrates Dailymotion videos into your WordPress site.


## Description

The Dailymotion Pro WordPress plugin supports your editorial workflow by facilitating the embedding of Dailymotion videos. You can import playback settings from your Dailymotion account and easily manage video content across your WordPress site.


## Features

- Seamless integration with the WordPress Block Editor (Gutenberg)
- Classic Editor integration
- Shortcode support for embedding videos
- Per-post video settings
- Dailymotion account integration
- Support for both public and private videos
- Playlist embedding
- Customizable player settings


## Requirements

- WordPress 6.0 or higher
- PHP 7.4 or higher
- Active Dailymotion account (for accessing your videos)


## Installation

1. Download the Dailymotion Pro plugin ZIP file.
2. In your WordPress admin panel, go to **Plugins > Add New**.
3. Click **Upload Plugin**.
4. Click **Choose File** and select the downloaded ZIP file.
5. Click **Install Now**.
6. After installation, click **Activate Plugin**.

Once activated, you'll see a **Dailymotion Pro** menu item in your WordPress admin sidebar.


## Connecting Your Dailymotion Account

To access your Dailymotion videos and playlists:

1. Go to **Dailymotion Pro > Connection** in your WordPress admin.
2. Follow the instructions to connect your Dailymotion account.
3. Once connected, you'll be able to access your videos and playlists directly from the WordPress editor.


## Usage

### Block Editor (Gutenberg)

1. Create or edit a post/page.
2. Click the **+** button to add a new block.
3. Search for **Dailymotion** and select the block.
4. Click **Search Videos**.
5. Search for a video by title or browse your videos/playlists.
6. Select the video you want to embed.
7. Adjust settings in the block panel.
8. Save or publish your content.

### Classic Editor

1. Create or edit a post/page.
2. Click the **Dailymotion** button in the editor toolbar.
3. Search for a video or playlist.
4. Select the video you want to embed.
5. Click **Insert**.
6. Save or publish your content.

### Using Shortcodes

You can manually embed Dailymotion videos using the shortcode:

```
[dm-player videoid=“VIDEO_ID” videotitle=“Video Title”]
```

**Shortcode Attributes:**

- `videoid`: The ID of the public Dailymotion video
- `privatevideoid`: The ID of a private Dailymotion video
- `playlistid`: The ID of a Dailymotion playlist
- `videotitle`: The title of the video (displayed as caption)

**Example:**

```
[dm-player videoid=“x7zxy9p” videotitle=“My Awesome Video”]
```


## Configuration

### Per-Post Video Settings

1. Edit a post/page containing a Dailymotion video.
2. In the Gutenberg sidebar, click **Video Settings**.
3. Adjust settings like Player ID, Mute, Video Heading, and Video Title.

### Global Plugin Settings

1. Go to **Dailymotion Pro > Plugin Settings**.
2. Adjust default settings for Player ID, mute, video heading, and video title display.


## Screenshots

1. Dailymotion Pro block in the WordPress Block Editor
2. Video search interface
3. Video settings panel
4. Plugin settings page
5. Setup Wizard


## Changelog

### 2.0.0

- Refreshed plugin from version 1.0.0


## Upgrade Notice

### 2.0.0

Initial public release of the refreshed Dailymotion Pro WordPress plugin.


## Support

For support, please contact the plugin developers through the official support channels or visit the [Dailymotion Pro Documentation](https://github.com/Dailymotion-Pro-Services/Dailymotion-Pro-WP-Docs).


## Frequently Asked Questions

### Can I embed private videos?

Yes. Connect your Dailymotion account and use the `privatevideoid` attribute or select the video through the editor interface.

### Can I customize the player appearance?

Yes. Specify a Player ID in the video settings. Player configurations are managed in your Dailymotion account.

### Can I embed playlists?

Yes. Use the `playlistid` shortcode attribute or select a playlist through the editor interface.

### Is the plugin compatible with WordPress multisite?

The plugin should work with WordPress multisite installations, but some features may require additional configuration.

### How do I get support?

Contact the developers through the official support channels or visit the documentation site.


## Troubleshooting

### Video Not Displaying

1. Check your internet connection.
2. Verify that the video ID is correct.
3. Ensure the video is publicly available or that you have access to private videos.
4. Confirm that your Dailymotion account is properly connected.

### Player Settings Not Working

1. Make sure you've saved your post/page after changing settings.
2. Check if per-post settings are overriding global settings.
3. Clear your browser cache and reload the page.

