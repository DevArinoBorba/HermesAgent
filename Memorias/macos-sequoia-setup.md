# macOS Sequoia Dark — Setup no Pop!_OS 24.04 COSMIC

## Status de aplicacao automatica (por Hermes)

### Aplicado via terminal
- [x] Tema Dark ativo (`com.system76.CosmicTheme.Dark`)
- [x] Cor primaria: `#1E1E1E` (igual macOS Sequoia Dark)
- [x] Cor de accent: `#0A84FF` (azul macOS)
- [x] Frosted glass: Heavy (efeito translucido igual macOS)
- [x] Bordas arredondadas aumentadas (radius_m: 14px)
- [x] Dock: autohide, centralizado, opacidade 0.85, bordas arredondadas 16px, margem 6px
- [x] Panel (barra topo): expandido, tamanho XS, relogio centralizado
- [x] Wallpaper: Sequoia Dark oficial baixado em ~/Pictures/macOS-Walls/Sequoia-Dark.png
- [x] Icones: Papirus-Dark instalado
- [x] Fonte: Inter 13 configurada (substituta do SF Pro)
- [x] Script brain-sync criado em ~/Applications/brain-sync.sh

### Requer intervencao manual (fazer pela interface grafica)

#### 1. Aplicar Wallpaper
   COSMIC Settings → Desktop → Wallpaper → Add picture
   Caminho: ~/Pictures/macOS-Walls/Sequoia-Dark.png

#### 2. Aplicar icones Papirus-Dark
   COSMIC Settings → Desktop → Appearance → Icon theme → Papirus-Dark

#### 3. Fonte Inter
   COSMIC Settings → Desktop → Appearance → Font → Inter 13

#### 4. Frosted Glass
   COSMIC Settings → Desktop → Appearance → Style → ligar "Frosted" (translucencia)

#### 5. Launcher estilo Spotlight
   O COSMIC ja tem o Pop Launcher (tecla Super).
   Para mudcar o atalho para Alt+Space (igual Mac):
   COSMIC Settings → Keyboard → Shortcuts → System → Launcher = Alt+Space

#### 6. Botoes de janela (opcional - mais parecido com Mac)
   COSMIC Settings → Desktop → Window Management → Place controls on left

## Notas de restauracao
Se reinstalar em outra maquina, copiar os dirs:
- ~/.config/cosmic/ (todas as configuracoes do COSMIC)
- ~/Pictures/macOS-Walls/ (wallpapers)
- ~/Applications/ (scripts utilitarios)
- ~/HermesBrain/ (este repo = segundo cerebro)
