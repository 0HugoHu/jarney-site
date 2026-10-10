# Jarney Site

Public-only website assets for Jarney / 游点钱. No app source, user data, pairing codes, logs, or credentials belong in this site repository.

Uses the same static nginx / Unraid Docker Controller layout as `0HugoHu/cardugo-site` (MIT). English and Simplified Chinese, light/dark appearance, no external fonts or scripts, no website analytics. Browser language preference is stored only in localStorage.

## NAS deployment

Add the separate public site repository to the Unraid Docker Controller. Build and start with port 80 internally; use the controller's allocated host port. Route `jarney.hugohu.site` through the existing HTTPS tunnel to this new container. Keep Cardugo's existing container and domain untouched.

Public paths: `/`, `/support`, `/privacy`. Verify all three over HTTPS before filling App Store Connect URLs.

Local preview: `python3 -m http.server 8081 --directory site` (use `.html` paths in this Python preview). Production clean URLs are provided by nginx.

The website contact address is already public on the Cardugo website. Private Apple review telephone/email are not copied to this repository.
