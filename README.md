## Advan AI Gen Ultra ACPI Patch

### Fix Touchpad
1.
```shell
sudo mkdir -p /boot/acpi
sudo cp ~/acpi-fix/dsdt.aml /boot/acpi/
```
2. if using dracut
```shell
echo 'acpi_override="yes"' | sudo tee /etc/dracut.conf.d/99-acpi-override.conf
echo 'acpi_table_dir="/boot/acpi"' | sudo tee -a /etc/dracut.conf.d/99-acpi-override.conf
```

3. regenerate image
```shell
sudo dracut --regenerate-all --force
```
