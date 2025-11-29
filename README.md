# Firefox Policies for Linux

This repository contains custom policies for the Firefox web browser, primarily defined in the `policies/policies.json` file. These policies can be used to customize and lockdown various Firefox settings.

## Installation on Linux

To apply these policies on a Linux system, you need to place the `policies.json` file in the recommended global policies directory.

1.  **Ensure Firefox is closed.**
2.  **Create the policies directory:** If it doesn't already exist, create the `/etc/firefox/policies/` directory.
    ```bash
    sudo mkdir -p /etc/firefox/policies/
    ```
3.  **Copy the `policies.json` file:** Copy the `policies.json` file from this repository into the newly created policies directory.
    ```bash
    sudo cp policies/policies.json /etc/firefox/policies/
    ```
4.  **Restart Firefox:** The policies should now be applied. You can verify this by typing `about:policies` in the Firefox address bar.

### Suggestion for Easier Updates (Symlinking)

To make updating your policies easier, you can use a symbolic link (symlink). This way, when you pull new changes from this repository, the symlink will automatically point to the updated `policies.json` file.

1.  **Remove the copied `policies.json` (if it exists):**
    ```bash
    sudo rm /etc/firefox/policies/policies.json
    ```
2.  **Create a symbolic link:**
    ```bash
    sudo ln -sf "$(pwd)/policies/policies.json" /etc/firefox/policies/policies.json
    ```
    This command creates a symbolic link from the `policies.json` file in your cloned repository to the Firefox policies directory.

**Note:** Always ensure you understand the policies you are applying, as they can significantly alter Firefox's behavior. Refer to the official Mozilla documentation for more details on Firefox policies.