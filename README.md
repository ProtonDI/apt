## Usage

```bash
curl https://protondi.github.io/apt/pubkey.gpg | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/proxmox-release-bullseye.gpg
sudo tee /etc/apt/sources.list.d/protondi.list <<< "deb [signed-by=/etc/apt/trusted.gpg.d/proxmox-release-bullseye.gpg] https://protondi.github.io/apt bullseye main"
sudo apt update
```
