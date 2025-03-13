Alternative OS image for (Podman) Machine
=========================================

> [!NOTE] 
> Currently this works on Linux only, and can not directly be used with `podman machine init --image` yet. Instead, you
> need [`download_container_disk_image`](https://github.com/gbraad-dotfiles/upstream/issues/81#issuecomment-2720544026)
> which will be part of [my dotfiles](https://github.com/gbraad-dotfiles/upstream).


```bash
$ download_container_disk_image ghcr.io/gbraad-devenv/fedora/podman-machine-os ~/DiskImages/podman-machine.qcow2
$ sudo virt-install \
  --import \
  --name podman-machine \
  --memory 4096 \
  --vcpus 2 \
  --disk ~/DiskImages/podman-machine.qcow2 \
  --os-variant fedora-eln
```
