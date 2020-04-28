# GDIndex Customized version

### Installation

1. Install [rclone](https://rclone.org/)
2. Setup your Google Drive: https://rclone.org/drive/
3. Run `rclone config file` to find your `rclone.conf` location
4. Find `refresh_token` in your `rclone.conf`, and `root_folder_id` too(optionally).
5. Copy the content of [worker/dist/worker.js](worker/dist/worker.js) to CloudFlare Workers.
6. Fill `refresh_token`, `root_folder_id` and other options on the top of the script.
7. Deploy!

## Lite mode

This mode will serve a simple nginx-like directory listing, and it only work with one drive. `upload` will be ignored in this mode.

On the top of the script, change `lite: false` into `lite: true`, than thats all.

