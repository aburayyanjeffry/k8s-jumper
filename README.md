# ☸ Kubernetes Jumper (kj) and Sons!

Kubernetes Jumper (`kj`) is a lightweight command-line utility that makes it easy to switch between Kubernetes clusters and namespaces using an interactive `fzf` menu.

It is inspired by tools such as `kubectx` and `kubens`, but combines common workflows into a single, simple command.

The project now includes two companion scripts:

- `awss` — interactively browse and select profiles from `.aws/config`
- `sss` — interactively browse and select hosts from `.ssh/config`

All three tools use the same menu-based approach for quickly navigating configuration files.

---

## Tools

### ☸ `kj` — Kubernetes Jumper

Use `kj` to interactively switch between Kubernetes contexts and namespaces.
<img width="837" height="527" alt="image" src="https://github.com/user-attachments/assets/8b95f480-4529-422f-9902-51c93c1cb674" />


**Features:**

- Interactive Kubernetes context selection
- Interactive namespace selection
- Switch cluster and namespace in one workflow
- Display the current cluster and namespace
- Keyboard navigation using `j` and `k`
- Works with existing kubeconfig contexts

### ☁ `awss` — AWS Config Jumper

Use `awss` to interactively browse AWS configuration profiles defined in `.aws/config`.
<img width="837" height="266" alt="image" src="https://github.com/user-attachments/assets/08058139-ecf3-4688-8f2d-6940011d7c45" />

**Features:**

- Interactive AWS profile selection
- Reads configuration from `~/.aws/config`
- Quickly browse and select AWS profiles
- Uses the same menu-based workflow as `kj`

### 🔐 `sss` — SSH Config Jumper

Use `sss` to interactively browse hosts defined in `.ssh/config`.
<img width="837" height="310" alt="image" src="https://github.com/user-attachments/assets/89b3d63a-8f0c-4d67-bfef-6c145be40b9b" />

**Features:**

- Interactive SSH host selection
- Reads configuration from `~/.ssh/config`
- Quickly browse and select SSH hosts
- Uses the same menu-based workflow as `kj`

---

## Requirements

- `kubectl` — required by `kj`
- `openssh` — required by `sss`
- `aws-cli` — required by `awss`
- `fzf` — used by all interactive menus
- AWS configuration file (`~/.aws/config`) — required by `awss`
- SSH configuration file (`~/.ssh/config`) — required by `sss`

---

## Installation

Clone the repository:

```bash
git clone <your-repository-url>
cd <your-repository-directory>
```

Make the scripts executable:

```bash
chmod +x kj awss sss
```

Move them somewhere in your `PATH`, for example:

```bash
sudo mv kj awss sss /usr/local/bin/
```

Or, if you prefer to keep personal scripts in `~/bin`:

```bash
mkdir -p ~/bin
mv kj awss sss ~/bin/
```

Make sure `~/bin` is in your `PATH`.

---

## Usage

### Kubernetes

Run:

```bash
kj
```

Use:

- `j` — move down
- `k` — move up
- `Enter` — select

`kj` helps you quickly jump between Kubernetes contexts and namespaces.

### AWS

Run:

```bash
awss
```

Select an AWS profile from your `.aws/config`.

### SSH

Run:

```bash
sss
```

Select an SSH host from your `.ssh/config`.

---

## Configuration Files

The tools read from your existing configuration files.

### Kubernetes

```text
~/.kube/config
```

### AWS

```text
~/.aws/config
```

### SSH

```text
~/.ssh/config
```

No separate configuration database is required.

---

## Why "and Sons"?

Because `kj` started as Kubernetes Jumper — and now it has a couple of little brothers:

```text
        ☸ kj
       /    \
    ☁ awss  🔐 sss
```

One menu-based idea, three useful command-line tools.

---

## Philosophy

Keep it simple.

Instead of remembering long commands or repeatedly editing configuration files, use a small interactive menu to quickly find what you need.

**Jump. Select. Done.**

---

## License

BSD License
