# Home Assistant Guest Instance

![Home Assistant Guest Instance Logo](logo.png)

A streamlined second Home Assistant instance designed specifically for **limited-access scenarios** like guest use, dedicated kiosks, or testing environments. It runs completely separate from your main instance, but is pre-configured to easily link back for entity sharing.

---

## Features

* **Isolated Environment:** A dedicated, fully functional Home Assistant Core instance, ensuring any changes or configurations do not impact your main setup.
* **Guest-Ready:** Perfect for creating a dashboard with **limited entity visibility** (e.g., only common area lights or entertainment controls) for visitors.
* **Custom Port:** Runs on **port `8223`** by default instead of the standard `8123`, preventing port conflicts and providing a dedicated access point. This can be easily changed in the add-on configuration.
* **HACS Pre-installed:** **HACS** (Home Assistant Community Store) is pre-installed and ready to use, simplifying the process of adding integrations and frontend elements needed for the guest/secondary setup.
* **Main Instance Connectivity:** Designed to be easily integrated with your main Home Assistant instance using the **Remote HomeAssistant** integrations to selectively pull a limited set of entities for display.

---

## Installation

1.  Navigate to **Supervisor** -> **Add-on Store**.
2.  Click the **three vertical dots** in the top right corner and select **Repositories**.
3.  Add the URL of this repository: `https://github.com/jpcornil-git/HA-addons`
4.  The "Home Assistant Guest" add-on should now appear in the list.
5.  Click on the add-on and select **INSTALL**.
6.  **Start** the add-on.
7.  Connect to the Home Assistant Guest instance using port 8223 instead o 8123
8.  HACS is already downloaded,go directly to [Setup HACS integration](https://www.hacs.xyz/docs/use/configuration/basic/#to-set-up-the-hacs-integration)
9.  Install the [remote_homeassistant](https://github.com/custom-components/remote_homeassistant) integration on both guest and main homeassistant instance, update configuration.yaml file of the latter.
10. Add

*NB*: If required, the config directory of the guest instance can be accessed using the terminal addon of the main instance and is located in /addon_configs/<sha>_ha_guest

---

## Configuration

The primary configuration option is the listening port (default is 8223).

