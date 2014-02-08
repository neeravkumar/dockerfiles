FROM base/arch
MAINTAINER me@nero.im
ONBUILD RUN curl "https://www.archlinux.org/mirrorlist/?country=$(curl ipinfo.io/country 2>/dev/null)&protocol=http&ip_version=4&use_mirror_status=on"|sed 's/#S/S/'> /etc/pacman.d/mirrorlist
ONBUILD RUN pacman -Syu --noconfirm
