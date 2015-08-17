# Contributor: Alexsandr Pavlov <kidoz at mail dot ru>
pkgname=ruby-rack110
_gemname=rack
pkgver=1.1.0
pkgrel=2
pkgdesc="A Ruby Webserver Interface"
arch=(any)
url="http://rack.rubyforge.org"
license=('MIT')
depends=('ruby' 'rubygems')
provides=('ruby-rack')
conflicts=('ruby-rack' 'ruby-rack1xx')
source=(http://rubygems.org/downloads/${_gemname}-${pkgver}.gem)
noextract=(${_gemname}-${pkgver}.gem)
md5sums=('f5ff2d6d348f41bb3833847223f792ce')

build() {
  cd "${srcdir}"
  export HOME=/tmp
  local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"
  gem install --no-user-install --ignore-dependencies -i "${pkgdir}${_gemdir}" -n "${pkgdir}/usr/bin" ${_gemname}-${pkgver}.gem
}
