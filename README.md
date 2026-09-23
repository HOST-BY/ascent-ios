# ASCENT 0.9.2 for iPhone

Native iOS shell for a personal planner, habits, finances, notes and creative projects. Install with AltStore Classic.

Source code is in ASCENT-iPhone-source.zip. The root GitHub Actions workflow extracts it, tests file storage and builds an unsigned arm64 IPA. Run Actions → Build ASCENT for AltStore → Run workflow, then download ASCENT-iPhone-AltStore.

Version 0.8 adds a shared ASCENT account for Windows and iPhone using Supabase Auth and private snapshots. Client connection settings contain only a public publishable key. Account sessions are stored using Windows DPAPI or iOS Keychain; no credentials or personal records are included in the source.

Sync runs after edits, every 30 seconds while open, and when returning to the app. Independent row changes merge; concurrent edits to the same row require a choice and preserve a local conflict backup. First connection to existing cloud data requires an explicit choice. The current snapshot size limit is 45 MiB, including photos and audio. Timers and notification history remain device-local. Offline edits stay on the device.

Backend schema is in cloud/schema.sql inside the archive. An administrator creates the personal account in Supabase Authentication; email delivery is not configured. Both devices use the same account. Supabase dashboard login is separate.

Automated model, file-storage, merge and mock two-device tests do not replace testing sign-in and installation on the actual iPhone. No background iOS sync or background notifications are promised. Keep a JSON backup before updating or connecting an account.

Version 0.9 adds a manual crypto portfolio, transactions, watchlist, research ideas, day tasks and CoinDesk headlines. Public CoinGecko quotes support 26 assets in RUB and USD. Average acquisition cost includes fees; historical FX must be entered for cross-currency cost calculations. Missing basis is shown as unavailable. Sources may be unavailable or rate limited; cached quotes are marked with timestamps. No wallet report import, trading or guaranteed investment recommendations. Update both clients for the new section.

Version 0.9.1 adds ADI, PUMP, FF, ZEC, ENA, PEPE and bundled offline coin logos. Toncoin is displayed as GRAM while retaining its existing record identity. Avalanche quote mapping corrected. No screenshot balances or transactions are imported.

Version 0.9.2 adds eight tokenized stocks and ETFs: AMZNx, VTIx, SCHFx, GOOGLx, AAPLx, IEMGx, NVDAx and INTCx, with local icons and token quotes. Equity tokens are excluded from the cryptocurrency research screener.
