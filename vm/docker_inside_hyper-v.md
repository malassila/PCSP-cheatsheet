# Using Docker inside of a Hyper-V VM

To use Docker inside of a Hyper-V VM, you need to enable virtualization extensions on the host machine.

1. Open a PowerShell prompt as administrator on the host machine.
2. Run the following command to enable virtualization extensions for the VM:
    
```powershell
Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true
```
Replace `<VMName>` with the name of the Hyper-V VM.

3. Start the VM and install Docker inside of it.
4. You should now be able to use Docker inside of the VM.

### *Here are some helpful tips:*
Normally Docker will be set up with WSL 2, as it is more performant than the Hyper-V backend. However, WSL 2 does not play well inside of a Hyper-V VM. To use Docker inside of a Hyper-V VM, you need to set the Docker backend to Hyper-V when installing Docker.

### *Here are some helpful links:*
Microsoft's documentation on [Nested Virtualization](https://learn.microsoft.com/en-us/virtualization/hyper-v-on-windows/user-guide/enable-nested-virtualization)

Microsoft's documentation on [Docker Engine on Windows](https://learn.microsoft.com/en-us/virtualization/windowscontainers/manage-docker/configure-docker-daemon)
