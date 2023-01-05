# Systemd

## Referência

* Site Debian

  * [SystemD](https://wiki.debian.org/pt_BR/systemd) 

* Site Archlinux

  * [SystemD](https://wiki.archlinux.org/title/Systemd_(Português))

   ## Comandos do systemctl

    systemctl list-unit-files | grep enabled

    systemctl disable [UNIT]
    
    systemctl --failed
    
    systemctl status
    
    systemctl reset-failed
    
    systemctl status udev.service
    
    systemctl enable lightdm
    
    systemctl restart systemd-random-seed.service
    
    systemd-analyze blame
    
    systemctl list-units
    
    systemctl list-units --all
    
    systemctl list-dependencies  graphical.target
    
    systemctl list-units --all
    
    systemctl --state=not-found  --all
    
    systemctl mask cryptsetup.target
    
    systemctl unmask cryptsetup.target

    systemctl restart display-manager
    
    systemctl get-default
    
    graphical.target

    systemctl set-default graphical.target

    systemctl isolate multi-user.target
    
    systemctl isolate graphical.target
    
    systemctl isolate default

### Tempo de carregamento no boot de cada processo

        systemd-analyze
        systemd-analyze blame

> Listando serviços
- Listando units

      systemctl
- Serviços ativos

        systemctl list-units -t service
