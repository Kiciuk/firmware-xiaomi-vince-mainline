
pkgname=firmware-xiaomi-vince-mainline
pkgver=5
pkgrel=0
pkgdesc="Firmware for Xiaomi Redmi 5 Plus"
url="https://github.com/Kiciuk/proprietary_firmware_vince"
arch="aarch64"
license="proprietary"
options="!check !strip !archcheck"
_commit="259716dfa2ab71d314e431bea9afa92b8261c95e"
source="https://github.com/Kiciuk/proprietary_firmware_vince/archive/$_commit.zip"
builddir="$srcdir/proprietary_firmware_vince-$_commit"

_fwdir="/lib/firmware/postmarketos"

package() {
	# parent package is empty
	mkdir -p "$pkgdir"

	# modem firmware
	install -Dm644 modem/mba.mbn -t "$pkgdir/$_fwdir"
	install -Dm644 modem/modem.* -t "$pkgdir/$_fwdir"

	# video firmware
	install -Dm644 apnhlos/venus.* -t "$pkgdir/$_fwdir"

	# WiFi/BT firmware
	install -Dm644 apnhlos/wcnss.* -t "$pkgdir/$_fwdir"
	install -Dm644 firmware/wlan/prima/WCNSS_qcom_wlan_nv.bin -t "$pkgdir/$_fwdir"/wlan/prima

	# ADSP firmware
	install -Dm644 modem/adsp.* -t "$pkgdir/$_fwdir"

	# GPU firmware
	install -Dm644 apnhlos/a506_zap.* -t "$pkgdir/$_fwdir"
}

