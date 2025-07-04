# Local Scripts and Configurations

This folder contains ready-to-use scripts and configuration examples to help you connect to and manage your Self-Host SaaS K3s cluster from your local machine.

## Contents

- **sample_ssh_config**: Example SSH config for secure tunneling to your server and K3s API. Copy and adapt entries to your `~/.ssh/config` for easier SSH access and port forwarding.
- **create_kubectl_port_fwd.sh**: Shell script to start all recommended `kubectl port-forward` commands for accessing cluster UIs (Grafana, Prometheus, Longhorn, Harbor, ArgoCD) on your local machine. Run with `zsh` for convenience.

## Usage

1. **SSH Config**
   - Edit `sample_ssh_config` and replace placeholders with your server's IP.
   - Copy relevant sections to your `~/.ssh/config`.
   - Use `ssh k3s-tunnel` (or your chosen host alias) to open tunnels easily.

2. **Port Forwarding Script**
   - Make the script executable: `chmod +x create_kubectl_port_fwd.sh`
   - Run: `./create_kubectl_port_fwd.sh`
   - Access UIs at the printed local URLs.

---

**Note:**
If you are running test scripts (such as `run_test_vm.sh`), make sure to execute them from the project root or parent folder, e.g.:

```sh
./tests/run_test_vm.sh
```

---

Feel free to adapt these samples to your workflow or operating system. For more details, see the main project documentation.