# ASCENT for iPhone

Personal planner, habits, finance, notes and creative projects. Native iOS shell with local storage and a mobile interface. Prepared for AltStore Classic.

Source code is in `ASCENT-iPhone-source.zip`; it contains Native, Web, tests, build.sh and documentation. The Actions workflow extracts this package, runs model and storage checks, then builds an unsigned device IPA. AltStore signs it with your Apple ID during installation.

Run **Actions → Build ASCENT for AltStore → Run workflow**. Download the **ASCENT-iPhone-AltStore** artifact after a successful build.

No personal records, API keys or certificates are included. Cloud sync is not implemented; backups can be transferred between Windows and iPhone. On-device validation is still required after the first successful build.
