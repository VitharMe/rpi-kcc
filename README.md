# rpi-kcc
Docker for **Raspberry Pi** with KCC

Based on [https://github.com/ciromattia/kcc](https://github.com/ciromattia/kcc)
### But what does it do?
When you start the container, look for images in the path / data and convert them to .EPUB with KCC.
By default, they are scaled with the best possible quality and cover all the margins of the Ereader.
After creating the .EPUB, it is converted to MOBI with kindlegen.
For this, kindlegen must be emulated with qemu-i386, since there is no native version in ARM.
This makes it a slow process, but with excellent results :)
### How To run
Mount on /data the folder with the images.

> **KCC_DEVICE** (Available options)
> K1, K2, K34, K578, KDX, KPW, KV, KO, KoMT, KoG, KoGHD, KoA, KoAHD, KoAH2O, KoAO, KoF
For example: *KO as Kindle Oasis* or KoAO as *Kobo Aura ONE*.
```
    docker run --rm -e KCC_DEVICE='KO' -v `pwd`/files:/data/ vitharme/rpi-kcc
