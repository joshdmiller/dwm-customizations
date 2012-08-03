pkgname=dwm
pkgver=6.0
pkgrel=1
pkgdesc="A dynamic window manager for X"
url="http://dwm.suckless.org"
arch=('i686' 'x86_64')
license=('MIT')
depends=('libxinerama' 'pango')
options=(zipman)
provides=('dwm')
conflicts=('dwm-pango')
#_source=(http://dl.suckless.org/dwm/dwm-$pkgver.tar.gz
_source=('dwm-6.0.tar.gz'
        config.h)
_patches=(01-dwm-6.0-xft.diff
          02-dwm-6.0-pertag2.diff
          03-dwm-6.0-uselessgaps.diff
          04-dwm-6.0-systray.diff
          05-dwm-6.0-urgentcolor.diff
##          xx-statuscolors.diff
          06-dwm-6.0-monocle_fixes.diff
	 	  07-dwm-6.0-statusallmons.diff
          08-dwm-6.0-chat.diff
          09-dwm-6.0-no_title.diff
          10-dwm-6.0-XKeycodeToKeysym_fix.diff
          00-dwm-6.0-buildflags.diff)
source=(${_source[@]} ${_patches[@]})

build() {
  for PATCH in "${_patches[@]}"; do
    msg "${PATCH##*/}" && patch -Np1 -i "${startdir}/${PATCH##*/}"
  done

  cd $srcdir/$pkgname-$pkgver
  cp $srcdir/config.h config.h

  make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11 || return 1
  make PREFIX=/usr DESTDIR=$pkgdir install || return 1

  install -m644 -D LICENSE $pkgdir/usr/share/licenses/$pkgname/LICENSE && \
  install -m644 -D README $pkgdir/usr/share/doc/$pkgname/README
}
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'ba3ccf3bfdf658f69075896afcc866b1'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '809635c039c6afb85dbebff2f096296d'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'a7040adac21d7316d70598ebd0e939c1'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '21ea1e012c7731994b51876d054ad8b2'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'ddcb917a614e0527bd815e52f16008db'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'ddcb917a614e0527bd815e52f16008db'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'f876ab9e50289dd644a8177425b1f9d5'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '1c790e5822cd22662d9b32666c3aa255'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '40385d994e045599c036f9232207d326'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'ac3994835f54be05ccb306e874541d7c'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'f876ab9e50289dd644a8177425b1f9d5'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '2ee9a0a3073035c7650cf4d4267bea11'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '299524112e840deeffa7322fd7809b2b'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '56886b6798f907ffedbd5f28173d4a1e'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '60627b44ee515f484bfd512413b2a40e'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'f876ab9e50289dd644a8177425b1f9d5'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '4d7415124f8c59c8b43891134b496860'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '57225848b76e8a9c4ce4b48ec2f61b04'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'f876ab9e50289dd644a8177425b1f9d5'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'a718c014d16b72af0d4deb70afb0e372'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '0606e47418c1885946a2c0c5f200f6e2'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '739f82f11d31db503eb0a563b3d6c01e'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '8e870647afa1c69bbc2759b6916cafec'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '59b1dc883851b5937bb8dd8d965f8c6d'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '59b1dc883851b5937bb8dd8d965f8c6d'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         'fe7de294084eb42bfe2d66d8949f1420'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '59b1dc883851b5937bb8dd8d965f8c6d'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '59b1dc883851b5937bb8dd8d965f8c6d'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '22aab7da44e6ff1ed49d37391c0bda63'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '59b1dc883851b5937bb8dd8d965f8c6d'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '59b1dc883851b5937bb8dd8d965f8c6d'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '59b1dc883851b5937bb8dd8d965f8c6d'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '59b1dc883851b5937bb8dd8d965f8c6d'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         'a671271fa1a17c3278589a97f834fd33'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '59b1dc883851b5937bb8dd8d965f8c6d'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         'df05b7c2dec1514950d7a66e80869a14'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '59b1dc883851b5937bb8dd8d965f8c6d'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '7c3f21a2ce2a4e22b2ee5ba12ed59e4a'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '59b1dc883851b5937bb8dd8d965f8c6d'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         'd71212b4d662d6358af4502b5535630b'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '7a197b650905f2f88c8e70e6de1a81e4'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '59b1dc883851b5937bb8dd8d965f8c6d'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '59b1dc883851b5937bb8dd8d965f8c6d'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '59b1dc883851b5937bb8dd8d965f8c6d'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '4f4b7a3a4de56283a3769fb12242e9fe'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '39961dea8d029ff995f7fd7171573c46'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'a38aac49cc30c2c8f17a9217be8d2a32'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'fc07f135b8033d1bc14351360b240d34'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'b0ef7934a2a48eaa2952531bb0d8f4a5'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'bc33310029e3a9d83f9571d78dff68b1'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '28b35ffdcef1bc7e1252405cff12be23'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'c4e235b520009b7a08d127cb92d690c8'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '30879fa6d717a0b68efcaffa7c45ea52'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'f64207c32f5a8efd3c61abbda84492c0'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '25811c12c9f17ba7a05dca95d361d929'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         '131d29dc5b7823d20fd08c461899cd92'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
md5sums=('8bb00d4142259beb11e13473b81c0857'
         'f64207c32f5a8efd3c61abbda84492c0'
         'b05a6e87e97f2d6ce29615dc1675fd6a'
         '0eb41bf700c80fe53c4c664b4da164fc'
         'a98f282724e43df243e2bcfc0d38036e'
         '4c79e30086e40d4904785b816ac73241'
         '9f5929dac1b006eaa721039f365680d0'
         '5f0b7065e44b3aec0d5393c9833b7d0f'
         'aa1b23aca5b1339a88fc4a3a17dbed3f'
         'bf47c515c7dcd31923872ad42af3224a'
         '045b5455cdcb5a226e6baf921d913751'
         '715c20080e88580138cb0acf29f6362d'
         '27175d10e252cb39a40b331c4ba3b2ce')
