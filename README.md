# macos-setup
Setup de herramientas para desarrollar sitios sin docker en macOS (e instalación de otras herramientas de mi gusto)

## Instalar herramientas base
### Brew
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Ejecutar para activar brew
```
echo >> /Users/bredebs/.zprofile
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/bredebs/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```
### iTerm2
```
brew install --cask iterm2
```

### alternativa a istats 
```
brew install stats
```

### alternativa a sizeup
```
brew install --cask rectangle
```

## Herramientas de desarrollo
### Bash Completion
```
brew install bash-completion
```
### VS Code
```
brew install --cask visual-studio-code
```
### DNSMasq
```
brew install dnsmasq
```
#### Configuración
```
curl -L https://gist.githubusercontent.com/dtomasi/ab76d14338db82ec24a1fc137caff75b/raw/550c84393c4c1eef8a3e68bb720df561b5d3f175/dnsmasq.conf -o /opt/homebrew/etc/dnsmasq.conf
sudo curl -L https://gist.githubusercontent.com/dtomasi/ab76d14338db82ec24a1fc137caff75b/raw/550c84393c4c1eef8a3e68bb720df561b5d3f175/dev -o /etc/resolv.conf
```
#### Reinicio Servicios
```
sudo brew services restart dnsmasq
```
#### Test
```
dig testing.a.domain.that.should.point.to.localhost.dev @127.0.0.1
```
### PHP
```
brew install php
pecl install xdebug
```

### MySQL
```
brew install mysql
```
### Nginx
```
brew install nginx
```
### Nginx UI
Descargar último release de [NginxUI](https://github.com/0xJacky/nginx-ui?tab=readme-ov-file)
```
mkdir /Users/bredebs/apps/
mkdir /Users/bredebs/apps/nginxui/
cd /Users/bredebs/apps/nginxui/
tar -xf /Users/bredebs/Downloads/nginx-ui-macos-64.tar.gz
```
La primera ejecución de nginxui es recomendable hacerla como `root` para poder crear las carpetas necesarias
```
cd /Users/bredebs/apps/nginxui/
nginx-ui -config app.ini
```
### Control para Servicios
```
brew install swiftbar
mkdir /Users/bredebs/apps/swiftbar/
cd /Users/bredebs/apps/swiftbar/
curl -L https://gist.githubusercontent.com/bredecl/20ab851603f6383a14158e8eb6ccaa5c/raw/9863fb88c83f617e4423c4310c456ea490e4c583/mempd.5s.sh -o /Users/bredebs/apps/swiftbar/mempd.5s.sh
```
