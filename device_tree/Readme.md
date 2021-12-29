
```
dtc -o dtb -o rpitx.dtbo -@ ./rpitx.dts

rmmod uio_pdrv_genirq
dtoverlay -R rpitx
dtoverlay ./rpitx.dtbo
modprobe uio_pdrv_genirq of_id=rpitx

ls /dev/uio*
ls /proc/device-tree/rpitx/

```
