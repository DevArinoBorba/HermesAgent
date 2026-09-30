# macOS Sequoia Dark — Setup Completo no Pop!_OS 24.04 COSMIC

## 1. Modificações Visuais Aplicadas Diretamente

- **Tema de Janelas e Cores:**
  - Base: `#1E1E1E` (Dark Grey estilo macOS)
  - Acento: `#0A84FF` (Azul clássico da Apple)
  - Frosted Glass (Blur): Ativado em modo Heavy
  - Raio dos cantos arredondados: Estilo macOS (radius_m: 14px)
  - Botões de janelas (GTK): Controles no lado esquerdo (`close,minimize,maximize:`)

- **Ícones e Cursores:**
  - Tema de Ícones: **WhiteSur-dark** (cópia fiel dos ícones do macOS Big Sur / Sonoma / Sequoia)
  - Tema de Cursor: **WhiteSur-cursors** (cursor oficial do macOS)
  - Tema GTK legado: **WhiteSur-Dark-blue** instalado em `~/.themes` e configurado no GTK 3/4.

- **Dock Inferior:**
  - Centralizado, flutuante (não expande até as bordas).
  - Opacidade: 0.85 com cantos arredondados (16px).
  - Configurado como App Dock limpo (Launcher + AppList + Minimizados).
  - Auto-ocultação inteligente (OnDemand).

- **Barra Superior (Panel):**
  - Fixa no topo (estilo Menu Bar do Mac).
  - Relógio e data centralizados.
  - Botões de apps/workspaces à esquerda (substituindo o menu Apple).
  - Centro de controle / status à direita (Áudio, Wi-Fi, Bluetooth, Bateria, Notificações).

- **Papel de Parede:**
  - Wallpaper oficial do **macOS Sequoia Dark** baixado em alta resolução em `~/Pictures/macOS-Walls/Sequoia-Dark.png`.

---

## 2. Ajustes Finais no COSMIC Settings (Interface Gráfica)

Para ativar os novos ícones e tema nas janelas nativas do COSMIC:

1. Abra **COSMIC Settings** (Super / Tecla Windows e digite "Settings").
2. Vá em **Desktop** → **Appearance**:
   - **Icon theme:** Escolha **WhiteSur-dark**.
   - **Cursor:** Escolha **WhiteSur-cursors**.
3. Vá em **Desktop** → **Window Management**:
   - Marque a opção para posicionar os botões de controle na **esquerda** (Place controls on left).
