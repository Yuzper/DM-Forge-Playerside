DM-Forge player site.

This folder is a complete static site: index.html plus assets/, one
encrypted bundle per player in data/, and the images they reference in
images/. Host it anywhere that serves static files (GitHub Pages works)
and give each player their username and password.

Per-player content is encrypted with PBKDF2-SHA256 + AES-256-GCM. Images
are NOT encrypted — they are ordinary files under images/, protected only
by unguessable filenames and the host not listing directories.

Republish into this same folder: the export prunes bundles and images it
no longer produces, which is what keeps revoked content from lingering.

Do not edit by hand.
