# rpi-kcc
Docker for **Raspberry Pi** with KCC

Based on [https://github.com/ciromattia/kcc](https://github.com/ciromattia/kcc)

### How To run
Mount on /data the folder with the images.

> **KCC_DEVICE** (Available options)
> K1, K2, K34, K578, KDX, KPW, KV, KO, KoMT, KoG, KoGHD, KoA, KoAHD, KoAH2O, KoAO, KoF
For example: *KO as Kindle Oasis* or KoAO as *Kobo Aura ONE*.
```
    docker run --rm -e KCC_DEVICE='KO' -v `pwd`/files:/data/ vitharme/rpi-kcc
