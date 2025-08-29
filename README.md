# Dailymotion Pro

**Contributors:** Dailymotion Profesional Services
**Tags:** video player, dailymotion, video, embed, media  
**Requires at least:** WordPress 6.0  
**Tested up to:** WordPress 6.8.2
**Stable tag:** 2.2.0
**Requires PHP:** 7.4  
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


## Installation

1. Download the Dailymotion Pro plugin ZIP file.
2. In your WordPress admin panel, go to **Plugins > Add New**.
3. Click **Upload Plugin**.
4. Click **Choose File** and select the downloaded ZIP file.
5. Click **Install Now**.
6. After installation, click **Activate Plugin**.

Once activated, you'll see a **Dailymotion Pro** menu item in your WordPress admin sidebar.


## Store Your Dailymotion Private API Key and API Secret

To access your Dailymotion videos and playlists:

1. Go to Dailymotion Pro > Connection in your WordPress admin Dashboard
2. Go to [Dailymotion Studio](https://www.dailymotion.com/partner/api-keys/) to generate a new private API key and API secret
3. Click "Create API Key" and choose Private API Key.
4. Permissions needed by the plugin:
	- Upload videos
	- Read videos
	- Read players
	- Read playlists
	- Read Channels
5. Find your channel name by visit [profiles page](https://www.dailymotion.com/partner/account/profiles) in Dailymotion Studio. You should see `@username`. Use it without `@`. E.g. `@myusername` > `myusername`
6. Once a private API key and API secret are stored, you'll be able to access your videos and playlists directly from the WordPress editor


## Configuration

### Per-Post Video Settings

1. Edit a post/page containing a Dailymotion video.
2. In the Gutenberg sidebar, click **Video Settings**.
3. Adjust settings like Player ID, Mute, Video Heading, and Video Title.

### Global Plugin Settings

1. Go to **Dailymotion Pro > Plugin Settings**.
2. Adjust default settings for Player ID, mute, video heading, and video title display.


## Auth Key

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


## Source Code and Development

This plugin includes minified JavaScript files that are built from TypeScript source code. In accordance with WordPress plugin guidelines, the source code is included in the plugin package in the `src` directory for JavaScript and in the `styles` directory for CSS.

The plugin uses the following build tools:
- npm: For JavaScript dependency management and build scripts
- webpack: For bundling and minifying JavaScript files
- TypeScript: For type-safe JavaScript development

To build the plugin from source:
1. Install dependencies: `npm install`
2. Build the JavaScript files: `npm run build`


## External Service

This plugin connects to the **Dailymotion API** as an external service. The API is used for:

- **Searching videos**: Search for both public and private content hosted on Dailymotion.
- **Private content access**: To access private videos, the plugin requires storing an API Key and API Secret securely in your WordPress installation.
- **Video information retrieval**: The API also provides video metadata (title, thumbnail, etc.) which is used to embed videos seamlessly into the WordPress editor.

By using this plugin, you acknowledge that interactions with the Dailymotion API are subject to Dailymotion's own policies and service conditions.

- [Terms of Use](https://legal.dailymotion.com/en/terms-of-use/)
- [Privacy Policy](https://legal.dailymotion.com/en/privacy-policy/)


## Support

For support, please contact the plugin developers through the official support channels or visit the [Dailymotion Pro Documentation](https://github.com/Dailymotion-Pro-Services/Dailymotion-Pro-WP-Docs/issues).


