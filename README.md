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
- PHP 8.0 or higher
- Active Dailymotion account (for accessing your videos)

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


= Auth Key =

**What is the Auth Key?**

The Auth Key is a security feature in the Dailymotion Pro plugin that protects your Dailymotion account credentials. Think of it as a special password that encrypts your sensitive information when it's stored in your WordPress database.

**Why is it Important?**

When you connect your WordPress site to Dailymotion, you need to store API credentials (similar to a username and password). The Auth Key ensures this information is securely encrypted, preventing unauthorized access to your Dailymotion account.

**How it Works for Users**

Automatic Protection

By default, the Dailymotion Pro plugin uses WordPress's built-in security keys to protect your information. This means:

- You don't need to do anything special to enable basic protection
- Your credentials are automatically encrypted when saved
- The plugin handles all the security details behind the scenes

Enhanced Security (Optional)

For users who want extra security, you can set up custom security keys:

1. **Generate secure random keys**: Use an online secure key generator
2. **Add the keys to your wp-config.php file**: Add the following lines near the other WordPress security keys:

```php
define('DM_PRO__AUTH_KEY', 'your-custom-random-key-here');
define('DM_PRO__NONCE_KEY', 'another-custom-random-key-here');
```

3. **Save the file**: Make sure to keep a backup of these keys in a secure location

**Best Practices**

- **Use unique keys**: Don't reuse passwords or keys from other services
- **Keep your wp-config.php secure**: Restrict access to this file on your server
- **Update keys periodically**: Consider changing your custom keys every few months for maximum security
- **Backup before making changes**: Always backup your site before editing configuration files


## User roles

We follow the <a href="https://wordpress.org/documentation/article/roles-and-capabilities/">roles and capabilities documentation</a> provided by the WordPress team.

**Super admin**
As a `Super Admin`, you can see and use the dailymotion plugin (all options: log in, credentials, settings) and search box/embed options

**Administrator**
As an `Admin`, you can see and use the dailymotion plugin (all options: log in, credentials, settings) and search box/embed options

**Editor**
As an `Editor`, you can see and use the dailymotion plugin (all options: log in, credentials, settings) and search box/embed options

**Author**
As an `Author`, you can see and use the dailymotion plugin (limited options: log in, manual embed settings access) and search box/embed options

**Contributor**
As a `Contributor`, you can see and use the dailymotion plugin (limited options: log in, manual embed settings access) and search box/embed options



## Installation

1. Download the Dailymotion Pro plugin ZIP file.
2. In your WordPress admin panel, go to **Plugins > Add New**.
3. Click **Upload Plugin**.
4. Click **Choose File** and select the downloaded ZIP file.
5. Click **Install Now**.
6. After installation, click **Activate Plugin**.

Once activated, you'll see a **Dailymotion Pro** menu item in your WordPress admin sidebar.


## Store Your Dailymotion Private API Key and Secret

To access your Dailymotion videos and playlists:

1. Go to Dailymotion Pro > Connection in your WordPress admin Dashboard
2. Go to [Dailymotion Studio](https://www.dailymotion.com/partner/api-keys/) to generate a new private API key and API secret
3. Click "Create API Key" and choose Private API Key.
4. Once a private API key and API secret are stored, you'll be able to access your videos and playlists directly from the WordPress editor


## Screenshots

1. Dailymotion Pro block in the WordPress Block Editor
2. Video search interface
3. Video settings panel
4. Plugin settings page
5. Setup Wizard


## Changelog

### 2.0.0

- Refreshed plugin from version 1.0.0. All-features list is available in the description


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

### If you experience issues after adding custom keys

1. **Check for typos**: Make sure the code was added exactly as shown
2. **Verify file permissions**: The wp-config.php file should have proper permissions (typically 644)
3. **Clear cache**: Clear your WordPress cache after making changes
4. **Contact support**: If problems persist, reach out to the plugin support team

