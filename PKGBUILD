# Contributor: John D Jones III <j[nospace]n[nospace]b[nospace]e[nospace]k[nospace]1972 -_AT_- the domain name google offers a mail service at ending in dot com>
# Generator  : CPANPLUS::Dist::Arch 1.27

pkgname='perl-module-manifest'
pkgver='1.08'
pkgrel='1'
pkgdesc="Parse and examine a Perl distribution MANIFEST file"
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl-params-util>=0.10' 'perl>=5.5.30' 'perl-file-slurp-tiny')
makedepends=()
checkdepends=('perl-test-exception>=0.27' 'perl-test-warn>=0.11')
url='http://search.cpan.org/dist/Module-Manifest'
source=('http://search.cpan.org/CPAN/authors/id/A/AD/ADAMK/Module-Manifest-1.08.tar.gz')
md5sums=('90f035a0074c3edcf8f595a38ec90da1')
sha512sums=('bd0793925a3dfbd1c15b98c8e41dd6e760d8d4be38711830af0a7f0f652706601be30328ec5522c137541dc00372ff3bfa56e8f5f02ea18d597284851a84e57c')
_distdir="Module-Manifest-1.08"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$srcdir/$_distdir"
    /usr/bin/perl Makefile.PL
    make
  )
}

check() {
  cd "$srcdir/$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    make test
  )
}

package() {
  cd "$srcdir/$_distdir"
  make install

  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
