FROM base/arch
MAINTAINER me@nero.im
RUN curl "https://www.archlinux.org/mirrorlist/?country=$(curl ipinfo.io/country 2>/dev/null)&protocol=http&ip_version=4&use_mirror_status=on"|sed 's/#S/S/'> /etc/pacman.d/mirrorlist
RUN pacman -Syu --noconfirm
ONBUILD pacman -Syu --noconfirm
