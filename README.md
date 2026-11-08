# Kamil App Store for umbrelOS

A community app store for [umbrelOS](https://umbrel.com). It packages self-hosted apps that are not (yet) in the official Umbrel App Store.

## Apps

| App | Version | Port | Upstream |
| --- | --- | --- | --- |
| BookOrbit | 3.7.0-1 | 2665 | [bookorbit/bookorbit](https://github.com/bookorbit/bookorbit) |

## Add this store to your Umbrel

1. Open the App Store on your Umbrel.
2. Open the menu in the top right and choose **Community App Stores**.
3. Paste `https://github.com/kamilnader/umbrel-app-store` and click **Add**.
4. Open **Kamil App Store** and install an app.

Community app stores are not reviewed by the Umbrel team. Only add stores from people you trust.

## BookOrbit notes

- First run: open BookOrbit and paste the password Umbrel shows for the app into the **Setup token** field, then create your own admin account.
- Your books live in the app's `data/books` folder by default. To use an existing folder, open the app's settings in Umbrel and change **Books library**. It shows up in BookOrbit as `/books`.
- Book requests: to import finished downloads, set **Downloads** in the app's Umbrel settings to the same folder your download client saves to. It shows up in BookOrbit as `/downloads`. Inside BookOrbit, reach other Umbrel apps by their container name, for example `http://prowlarr_server_1:9696` and `transmission_server_1:9091`, with **Allow private addresses** turned on.
- If you open BookOrbit at an address other than `http://umbrel.local:2665` (for example over Tailscale or HTTPS), set `APP_URL` in the app's Umbrel settings so Kobo links, emails and live updates use it.
- The Umbrel login protects the web UI. Paths under `/api/` are left open so Kobo, KOReader, OPDS readers and the BookOrbit iPhone app can connect; BookOrbit checks its own credentials on those routes.

## License

The packaging files in this repository are provided as-is. Each app keeps its own license.

BookOrbit is licensed under the GNU Affero General Public License, version 3 only, with [additional terms](https://github.com/bookorbit/bookorbit/blob/main/ADDITIONAL_TERMS.md). This store runs the unmodified upstream image and does not change BookOrbit. Its attribution notice:

> [Powered by BookOrbit](https://github.com/bookorbit/bookorbit)
> Copyright (C) 2025-2026 neon.
> Additional copyright is held by the respective BookOrbit contributors.
> Original project: https://github.com/bookorbit/bookorbit
