# pmai-launcher
PROMETEO Multimodal Artificial Intelligence Launcher Repository 

## ⚙️ Configuración Inicial

### 1. Configurar Submódulos

**Primera vez - Inicializar submódulos:**

```bash
git submodule update --init --recursive
```

**Actualizar referencias a los submódulos:**

```bash
git submodule update --remote
```

### 2. Configuracion de camaras

https://learn.microsoft.com/en-us/windows/wsl/connect-usb
https://www.youtube.com/watch?v=t_YnACEPmrM

winget install --interactive --exact dorssel.usbipd-win


wsl --shtudown
usbipd list

usbipd bind --busid <Bus de las camaras>
usbipd bind --busid 2-2

usbipd list // Verificar shared

// Abrir una terminal ubuntu para mantener la wsl activa

usbipd attach --wsl --busid <busid>
usbipd attach --wsl --busid 2-2

ls -al /dev/video*


sudo apt update && sudo apt upgrade -y && sudo apt install -y build-essential flex bison libgtk2.0-dev libelf-dev libncurses-dev autoconf libudev-dev libtool zip unzip v4l-utils libssl-dev python3-pip cmake git iputils-ping net-tools dwarves


# Probar la camara WSL/Linux
sudo apt install v4l-utils guvcview
sudo guvcview