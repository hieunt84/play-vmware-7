### Intro
```
Mục tiêu là gì: chuẩn bị môi trường lab VMware Vsphere 7
Storage: San Truenas
ESXi
Vcenter
```

### Ref
```
https://www.nakivo.com/blog/vmware-vsphere-7-installation-setup/
```

### Prepare
```
https://cuongquach.com/download-vmware-vsphere-7-iso.html
1. Install Vmware Workstation 16
2. download
- ESXi 7 /dell/hp
- Vcenter 7
3. find license free
```

### Step01 : deploy truenas
```
01 x Truenas:172.20.10.130/root/Hit@2022
  -add disk 1TB for Vmware Vcenter
root/Hit@2022
```

### Step02 : deploy esxi
```
https://www.nakivo.com/blog/vmware-vsphere-7-installation-setup/
02 x ESXi: 8vcpu, 16GB Ram 
  Esxi1: 172.20.10.128
  Esxi2: 172.20.10.129
root/Hit@2022
- add 1 VMkernic to connect iscsi
ref: https://ratticon.com/tutorial-how-to-set-up-iscsi-for-esxi-on-freenas-11-2/

```

### Step03 : deploy vcenter
```
https://www.nakivo.com/blog/vmware-vsphere-7-installation-setup/
01 vcenter: 172.20.10.132
root/Hit@2022
administrator@vsphere.local/Hit@2022
- ref: images/info-setup-vcenter.png
- add license
- create datacenter: dc1
- add host esxi
- create cluster
- add host to cluster
- create folder k8s
- add cluster to k8s

```
