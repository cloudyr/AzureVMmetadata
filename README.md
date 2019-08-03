# AzureVMmetadata

A simple package to access the instance metadata service in an Azure virtual machine.

## Accessing metadata

AzureVMmetadata exposes 3 environments that contain the instance metadata for the VM:

- `instance`: The instance metadata, containing 2 components: `compute` and `network`
- `attested`: The attested metadata, containing the PKCS-7 certificate for the VM
- `events`: The scheduled events for the VM

The first two are automatically populated when the package is loaded; you can also manually update them with the `update_instance_metadata()` and `update_attested_metadata()` functions. `events` is not populated, but you can update it manually with `update_scheduled_events()`.

----
<p align="center"><a href="https://github.com/Azure/AzureR"><img src="https://github.com/Azure/AzureR/raw/master/images/logo2.png" width=800 /></a></p>
