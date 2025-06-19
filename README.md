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
curl -L https://gist.githubusercontent.com/dtomasi/ab76d14338db82ec24a1fc137caff75b/raw/550c84393c4c1eef8a3e68bb720df561b5d3f175/dnsmasq.conf -o /usr/local/etc/dnsmasq.conf
sudo curl -L https://gist.githubusercontent.com/dtomasi/ab76d14338db82ec24a1fc137caff75b/raw/550c84393c4c1eef8a3e68bb720df561b5d3f175/dev -o /etc/resolver/dev
```
#### Reinicio Servicios
```
sudo brew services restart dnsmasq
```
#### Test
```
dig testing.a.domain.that.should.point.to.localhost.dev @127.0.0.1
```



