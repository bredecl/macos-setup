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
