# Deskripsi Kernel

Lihat Deskripsi Cina |  [查看中文说明](readme.cn.md)
Lihat Deskripsi indonesa |  [查看中文说明](readme.ID.md)

Kernel ini dapat digunakan untuk sistem `armbian` dan` openwrt`, seperti [amlogic-s9xxx-armbian](https://github.com/ophub/amlogic-s9xxx-armbian), [amlogic-s9xxx-openwrt](https://github.com/ophub/amlogic-s9xxx-openwrt), [flippy-openwrt-actions](https://github.com/ophub/flippy-openwrt-actions), dan [Unifreq/openwrt_packit](https://github.com/unifreq/openwrt_packit) proyek. Mereka dapat diintegrasikan saat menyusun firmware atau diinstal dalam sistem yang ada. Di antara mereka, [kernel_flippy](https://github.com/ophub/kernel/releases/tag/kernel_flippy), [kernel_stable](https://github.com/ophub/kernel/releases/tag/kernel_stable), [kernel_dev](https://github.com/ophub/kernel/releases/tag/kernel_dev) dan [kernel_beta](https://github.com/ophub/kernel/releases/tag/kernel_beta) adalah interchangeable umum. Untuk metode penggunaan khusus, lihat instruksi [Kernel Gunakan](https://github.com/ophub/amlogic-s9xxx-armbian/tree/main/compile-kernel).

- File kernel di [kernel_flippy](https://github.com/ophub/kernel/releases/tag/kernel_flippy) dari rilis adalah `versi stabil`, yang merupakan kernel seri yang dibagikan oleh` flippy`.
- File kernel di [kernel_stable](https://github.com/ophub/kernel/releases/tag/kernel_stable) dari rilis adalah `versi stabil`, yang telah memungkinkan lebih banyak opsi dukungan sesuai dengan kebutuhan pengguna.
- File kernel di [kernel_dev](https://github.com/ophub/kernel/releases/tag/kernel_dev) dari rilis adalah `Versi Pengembangan`, yang menambahkan dukungan driver pihak ketiga dan modifikasi khusus untuk beberapa kotak tertentu.
- File kernel di [kernel_beta](https://github.com/ophub/kernel/releases/tag/kernel_beta) dari rilis adalah `versi beta`, yang mendukung penambahan kustom patch driver pihak ketiga, dan memungkinkan kompilasi konfigurasi khusus.
- File kernel di [kernel_rk3588](https://github.com/ophub/kernel/releases/tag/kernel_rk3588) bagian rilis adalah `versi khusus` untuk seri` RK3588`, dan mereka tidak kompatibel dengan seri lainnya.
- File kernel di [kernel_rk35xx](https://github.com/ophub/kernel/releases/tag/kernel_rk35xx) bagian rilis adalah `versi khusus untuk` rk3528/rk3566/rk3568 `rk3528 mereka tidak, rk3528/rk3566/rk3568`
- File kernel di [kernel_h6](https://github.com/ophub/kernel/releases/tag/kernel_h6) dari rilis adalah `versi khusus` untuk` allwinner h6(tqc-a01) `perangkat, dan mereka tidak kompatibel dengan seri lain.
- Bagian [dev](https://github.com/ophub/kernel/releases/tag/dev) dalam rilis memiliki gambar unduhan `cross-compilation toolchain` yang diperlukan saat menyusun kernel.
- [S905X4](https://github.com/dirgha80/kernel/releases/tag/s905x4) Khusus amlogic S905x4
- Bagian [alat](https://github.com/ophub/kernel/releases/tag/tools) dalam rilis telah mengunduh gambar `sistem android` untuk beberapa kotak TV umum, yang dapat digunakan untuk mengembalikan sistem Android saat menggunakan sistem Armbian dan OpenWRT.


## Kompilasi Kernel ##

-Untuk metode kompilasi kernel, silakan merujuk ke [Compile-Kernel](https://github.com/ophub/amlogic-s9xx-armbian/tree/main/compile-kernel). Untuk metode kompilasi kernel menggunakan tindakan di github.com, lihat [.github/alur kerja](. GitHub/alur kerja). Anda dapat menyesuaikan kernel dengan memodifikasi file konfigurasi kernel di [kernel-config](kernel-config), dan tambahkan tambalan kernel khusus di direktori [kernel-patch](kernel-patch).

- Anda dapat menyesuaikan konfigurasi kernel sesuai dengan kebutuhan Anda, seperti menambahkan driver dan tambalan. Anda juga dapat menyusun kernel tanda tangan yang dipersonalisasi dengan makna khusus sesuai dengan suasana hati Anda, seperti `5.10.95-Happy-new-year`,` 5.10.96-beijing-winter-olympics`, `5.10.99-valentines-day`, dll.

- Nama: Kompilasi kernel
  Penggunaan: Ophub/amlogic-s9xxx-mrembian@main
  dengan:
    build_target: kernel
    Kernel_version: 5.10.135_5.15.50
    Kernel_auto: Benar
    Kernel_Sign: -yyourname
`` `

## Kode Sumber Kernel ##

Terima kasih banyak untuk Unifreq dan lainnya karena telah mempertahankan kode sumber kernel. Kode sumber yang digunakan dalam file kernel di repositori adalah sebagai berikut:

| Tag kernel | Repositori Kode Sumber | Perangkat yang berlaku |
| ------------- | ----------------------- | ----------------------- |
| [kernel_flippy](https://github.com/ophub/kernel/releases/tag/kernel_flippy)<br>[kernel_stable](https://github.com/ophub/kernel/releases/tag/kernel_stable)<br>[kernel_dev](https://github.com/ophub/kernel/releases/tag/kernel_dev)<br>[kernel_beta](https://github.com/ophub/kernel/releases/tag/kernel_beta) | [unifreq/linux-5.4.y](https://github.com/unifreq/linux-5.4.y)<br>[unifreq/linux-5.10.y](https://github.com/unifreq/linux-5.10.y)<br>[unifreq/linux-5.15.y](https://github.com/unifreq/linux-5.15.y)<br>[unifreq/linux-6.1.y](https://github.com/unifreq/linux-6.1.y)<br>[unifreq/linux-6.6.y](https://github.com/unifreq/linux-6.6.y)<br>[unifreq/linux-6.12.y](https://github.com/unifreq/linux-6.12.y) | Amlogic<br>Allwinner<br>Rockchip |
| [kernel_rk3588](https://github.com/ophub/kernel/releases/tag/kernel_rk3588) | [unifreq/linux-5.10.y-rk35xx](https://github.com/unifreq/linux-5.10.y-rk35xx) | Rockchip-RK3588 |
| [kernel_rk35xx](https://github.com/ophub/kernel/releases/tag/kernel_rk35xx) | [unifreq/linux-5.10.y-rk35xx](https://github.com/unifreq/linux-5.10.y-rk35xx) | Rockchip-RK3528/RK3566/RK3568 |
| [kernel_h6](https://github.com/ophub/kernel/releases/tag/kernel_h6) | [13584452567/linux-6.4.y](https://github.com/13584452567/linux-6.4.y)<br>[13584452567/linux-6.5.y](https://github.com/13584452567/linux-6.5.y)<br>[13584452567/linux-6.6.y](https://github.com/13584452567/linux-6.6.y) | Allwinner-H6(TQC-A01) |
| [kernel_stable](https://github.com/ophub/kernel/releases/tag/kernel_stable)<br>[kernel_dev](https://github.com/ophub/kernel/releases/tag/kernel_dev)<br>[kernel_h6](https://github.com/ophub/kernel/releases/tag/kernel_h6)<br>[kernel_rk3588](https://github.com/ophub/kernel/releases/tag/kernel_rk3588)<br>[kernel_rk35xx](https://github.com/ophub/kernel/releases/tag/kernel_rk35xx) | [codesnas/linux-5.4.y](https://github.com/codesnas/linux-5.4.y)<br>[codesnas/linux-5.10.y](https://github.com/codesnas/linux-5.10.y)<br>[codesnas/linux-5.15.y](https://github.com/codesnas/linux-5.15.y)<br>[codesnas/linux-6.1.y](https://github.com/codesnas/linux-6.1.y)<br>[codesnas/linux-6.6.y](https://github.com/codesnas/linux-6.6.y)<br>[codesnas/linux-6.12.y](https://github.com/codesnas/linux-6.12.y)<br>[codesnas/linux-h6-6.6.y](https://github.com/codesnas/linux-h6-6.6.y)<br>[codesnas/linux-5.10.y-rk35xx](https://github.com/codesnas/linux-5.10.y-rk35xx) | Kode sumber kernel dikloning dari repositori <br> [unifreq](https://github.com/unifreq), [13584452567](https://github.com/13584452567) dan [chewitt](https://github.com/chewitt/linux), | Kode sumber kernel dikloning dari repositori <br> dari [Unifreq](https://github.com/unifreq), [13584452567](https://github.com/1358452567) dan [chewitt](htttps:gllinix/gubux/gridps:gitps:gitps) untuk menambal kernel dengan mengikuti para ahli ini. |
| [kernel_rk3588](https://github.com/ophub/kernel/releases/tag/kernel_rk3588) | [Armbian/Linux-Rockchip](https://github.com/armbian/linux-rockchip) | Rockchip-beta(6.1.y) |
| [kernel_rk35xx](https://github.com/ophub/kernel/releases/tag/kernel_rk35xx) | [Armbian/Linux-Rockchip](https://github.com/armbian/linux-rockchip) | Rockchip-beta(6.1.y) |
| [kernel_s905x4](https://github.com/houjie80/kernel2/releases/tag/kernel_s905x4) | [Sibondt/Linux-6.1.66](https://github.com/sib0ndt/linux-6.1.66) <br> [houji80/linux-6.6.y](https://github.com/houji80/linux-6.6.y) <br> [houji80/linux-6.12.y](https://github.com/houuji80/linux-6.12.y) | Amlogic S905x4


## Tautan ##

- [Unifreq/Kernel](https://github.com/unifreq)
- [13584452567/kernel](https://github.com/13584452567/linux-6.4.y)
- [Chewitt/Linux](https://github.com/chewitt/linux)
- [torvalds/linux](https://github.com/torvalds/linux)
- [kernel.org](https://kernel.org)
- [Sibondt/Linux-6.1.66](https://github.com/sib0ndt/linux-6.1.66)
- [houji80/linux-6.12.y](https://github.com/houjie80/linux-6.12.y)
- [houji80/linux-6.6.y](https://github.com/houjie80/linux-6.6.y)

## Lisensi 

Kernel © Ophub dilisensikan di bawah [GPL-2.0](https://github.com/ophub/kernel/blob/main/license)
