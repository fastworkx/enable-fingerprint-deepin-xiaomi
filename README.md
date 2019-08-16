
# Habilitar fingerprint en Deepin con xiaomi air 13 - 2019

## Verificar el kernel reconocio el dispositivo
```
:~$ lsusb
Bus 002 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub
Bus 001 Device 005: ID 8087:0a2b Intel Corp.
Bus 001 Device 004: ID 04f3:0c1a Elan Microelectrnics Corp. <=== Este es 
Bus 001 Device 003: ID 04f2:b5a3 Chicony Electronics Co., Ltd 
Bus 001 Device 002: ID 1bcf:0005 Sunplus Innovation Technology Inc. Optical Mouse
Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
```

## Clonar el siguiente repositorio
git clone https://github.com/iafilatov/libfprint

## Seguir los pasos del repositorio e instalar
- `sudo apt install ninja-build`
- `sudo apt-get install build-essential`

## Tambien instalar 
instalar con `sudo apt install ...`
- libglib2.0-dev
- libnss3-dev
- libpixman-1-dev
- libusb-1.0.0-dev
- libx11-dev
- libxv-dev
- pkg-config

## para compilar e instalar la libreria

- `venv/bin/meson builddir`
- `venv/bin/meson configure builddir -Ddoc=false -Dlibdir=lib`
- `cd builddir`
- `ninja`
- `sudo ninja install`

## Finalmente ejecutar
`sudo ldconfig`
Para habilitar la libreria en la cache, luego cerrar sesion e iniciar de nuevo
Para probar si se reconoce el fingerprint desde linea de comandos probar con estos: 
- `fprintd-enroll` registra nueva huella digital
- `fprintd-list <user>` muestra huella digital registrada asociada a un user
- `fprintd-verify` verifica

## Bkp de comandos utilizados
fprintd-enroll 
  133  fprintd-verify 
  134  sudo ninja install
  135  apt policy libpam-fprintd
  136  fprintd-enroll
  137  apt policy libpam-fprintd
  138  apt policy fprintd
  139  which fprintd
  140  ls -la
  141  sudo apt install ninja-build
  142  cd ..
  143  python3 -m venv venv
  144  sudo apt-get install python3-venv
  145  python3 -m venv venv
  146  . venv/bin/activate
  147  pip install -U pip
  148  pip install meson
  149  cd builddir/
  150  sudo ninja install
  151  apt policy libusb-1.0.so
  152  apt policy libusb-1.0
  153  apt policy libfprint.so.0.0.0
  154  apt policy libfprint
  155  sudo apt install libusb-1.0.0-dev
  156  sudo ninja install
  157  sudo apt install libpixman-1-dev
  158  sudo ninja install
  159  libx11-dev
  160  sudo apt install libx11-dev
  161  sudo ninja install
  162  sudo apt install libxv-dev
  163  sudo ninja install
  164  sudo apt install pkg-config
  165  sudo apt install libnss3-dev
  166  sudo apt install libglib2.0-dev
  167  sudo apt install libusb-1.0.0-dev
  168  sudo apt install libpixman-1-dev
  169  sudo ninja install
  170  cd ..
  171  rm -rf builddir/
  172  meson builddir
  173  sudo apt-get install build-essential
  174  meson builddir
  175  meson configure builddir -Ddoc=false -Dlibdir=lib
  176  cd builddir/
  177  ninja
  178  sudo ninja install
  179  fprintd-enroll
  180  sudo cat /etc/ld.so.cache 
  181  sudo cat /etc/ld.so.conf
  182  ldconfig --help
  183  sudo ldconfig
  184  fprintd-enroll 
  185  fprintd-list 
  186  fprintd-list emerson
  187  fprintd-verify 
  188  fprintd-list emerson
  189  fprintd-enroll 
  190  sudo
  191  sudo ls
  192  fprintd-verify 
  193  fprintd-enroll 
  194  fprintd-verify 
  195  fprintd-enroll 
  196  fprintd-verify 

