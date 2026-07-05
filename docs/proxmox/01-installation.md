# Proxmox VE Installation

## Objective

Install Proxmox VE on the Dell Precision 5820 and prepare it as the virtualization host for my homelab.

---

## Hardware

- Host: Dell Precision 5820
- CPU: Intel Xeon W-2295
- Memory: 32 GB DDR4
- Storage: 512 GB NVMe SSD

---

## Installation Summary

- Downloaded the Proxmox VE ISO.
- Created a bootable USB installer.
- Installed Proxmox VE.
- Configured networking with a static IP.
- Logged into the Proxmox web interface.
- Created the initial storage configuration.

---

## Troubleshooting

### Issue: ISO Upload Failed

#### Symptoms

The RHEL 10 ISO upload failed immediately.

#### Root Cause

I selected an invalid local file path instead of the downloaded ISO which I thought I had since I already had an instance on VirtualBox. 


#### Resolution

- Went to Redhat Developer Portal.
- Verified the ISO download.
- Selected the correct file.
- Successfully uploaded the ISO.

#### Lessons Learned

Always verify the selected file before uploading to Proxmox.

---

## Next Steps

- Create RHEL 10 VM
- Register the VM
- Update the VM
