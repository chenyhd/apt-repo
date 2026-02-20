# APT Repository for essh

This repository hosts the APT package repository for [essh](https://github.com/chenyhd/essh), served via GitHub Pages.

## Setup

```bash
# Add the GPG key
curl -fsSL https://chenyhd.github.io/apt-repo/gpg.key | sudo gpg --dearmor -o /usr/share/keyrings/essh-archive-keyring.gpg

# Add the repository
echo "deb [signed-by=/usr/share/keyrings/essh-archive-keyring.gpg] https://chenyhd.github.io/apt-repo stable main" | sudo tee /etc/apt/sources.list.d/essh.list

# Install
sudo apt update
sudo apt install essh
```

## Update

```bash
sudo apt update && sudo apt upgrade essh
```

The repository is automatically updated when a new essh release is published.
