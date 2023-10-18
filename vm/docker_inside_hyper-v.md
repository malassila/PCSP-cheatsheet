# Using Docker inside of a Hyper-V VM

To use Docker inside of a Hyper-V VM, you need to enable virtualization extensions on the host machine.

1. Open a PowerShell prompt as administrator on the host machine.
2. Run the following command to enable virtualization extensions for the VM:
    
```powershell
Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true
```
Replace `<VMName>` with the name of your Hyper-V VM.

3. Start the VM and install Docker inside of it.
4. You should now be able to use Docker inside of the VM.

That's it! With virtualization extensions enabled, Docker should work seamlessly inside of your Hyper-V VM.
