# ☸ Kubernetes Jumper (kj)

Kubernetes Jumper (`kj`) is a lightweight command-line utility that makes it easy to switch between Kubernetes clusters and namespaces using an interactive `fzf` menu.

It is inspired by tools such as `kubectx` and `kubens`, but combines common workflows into a single command.

---

## Features

- Interactive cluster selection
- Interactive namespace selection
- Cluster + namespace switching in one command
- Display current cluster and namespace
- Keyboard navigation using `j` and `k`
- Works with existing kubeconfig contexts

---

## Requirements

- kubectl
- fzf

### Install fzf

Ubuntu / Debian:

```bash
sudo apt update
sudo apt install -y fzf
```

macOS (Homebrew):

```bash
brew install fzf
```

Verify installation:

```bash
kubectl version --client
fzf --version
```
---

## Installation

Make the script executable:

```bash
chmod +x kj
```

Optionally place it somewhere in your PATH:

```bash
sudo cp kj /usr/local/bin/kj
```

---

## Usage

### Switch Cluster

Select a Kubernetes cluster from your kubeconfig.

```bash
kj
```

Example:


<img width="782" height="375" alt="image" src="https://github.com/user-attachments/assets/936e2f82-bf9f-42f4-a667-365653c5d2b9" />



---

### Switch Namespace Only

Switch namespace within the current cluster.

```bash
kj -n
```

Example:


<img width="1100" height="407" alt="image" src="https://github.com/user-attachments/assets/ff4b857e-222b-46c7-a39e-e8dce896efa1" />


---

### Switch Cluster and Namespace

Select a cluster and then a namespace.

```bash
kj -a
```

Example:

<img width="781" height="753" alt="image" src="https://github.com/user-attachments/assets/721cd17e-e490-40ba-b639-5f36656a9c9f" />

---

### Show Current Selection

Display the currently active cluster and namespace.

```bash
kj -l
```

Example:

<img width="835" height="160" alt="image" src="https://github.com/user-attachments/assets/ecceca95-ba2b-46ee-907d-e2b971188f15" />



---

### Help

Display help information.

```bash
kj -h
```

---

## Keyboard Shortcuts

| Key | Action |
|------|---------|
| j | Move down |
| k | Move up |
| ↑ | Move up |
| ↓ | Move down |
| Enter | Select |
| Esc | Exit |

---

## Command Summary

```text
kj       Select cluster
kj -n    Select namespace only
kj -a    Select cluster then namespace
kj -l    Show current cluster and namespace
kj -h    Show help
```

---

## Author

Jeffry Johar

Built to simplify day-to-day Kubernetes navigation for DevOps engineers.
