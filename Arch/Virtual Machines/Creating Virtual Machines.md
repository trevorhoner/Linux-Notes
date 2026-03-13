# Creating Virtual Machines

## Cheatsheet   

- [] [**1.**]( #1-install-necessary-packages ) `sudo pacman -Syu qemu virt-manager libvirt dnsmasq ebtables iptables-nft`
- [] [**2.**]( #2-enable-libvirtd-system-service ) `sudo systemctl enable --now libvrtd`
- [] [**3.**]( #3-assign-user-privledges-to-virtual-manager ) `sudo usermod -aG libvirt trevor`


