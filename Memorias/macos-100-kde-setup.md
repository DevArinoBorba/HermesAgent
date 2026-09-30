# Setup 100% macOS Sequoia / Big Sur no Pop!_OS (via KDE Plasma)

## O que foi instalado e configurado automaticamente

1. **Ambiente KDE Plasma 5.27:**
   - Pacotes de desktop, wayland, workspace, rede, áudio e o gerenciador de arquivos Dolphin.
   - Sessões registradas: `Plasma (Wayland)` e `Plasma (X11)`.

2. **Tema Global WhiteSur-KDE (Dark):**
   - Aplicado via `lookandfeeltool -a com.github.vinceliuice.WhiteSur-dark --resetLayout`.
   - Layout automático:
     - **Painel Superior:** Barra de Menus Global (Arquivo, Editar, Exibir dos apps), Data/Hora centralizada e Ícones de Status/Controle na direita.
     - **Dock Inferior:** Centralizado e flutuante com indicadores e inicializador.

3. **Animação da Lâmpada Mágica (Magic Lamp):**
   - Ativada nativamente no `kwinrc`:
     - `magiclampEnabled=true` (Duração 350ms).
     - `blurEnabled=true` (Vidro fosco em menus e janelas).

4. **Botões de Janela (Controles da Apple):**
   - Posicionados na **esquerda** com tema WhiteSur-Dark:
     - `ButtonsOnLeft=XIA` (Fechar, Minimizar, Maximizar em estilo semáforo vermelho/amarelo/verde).

5. **Motor de Estilo Kvantum:**
   - Tema `WhiteSur` instalado e definido como padrão (`kvconfig`).

6. **Ícones, Cursores e Sons:**
   - Ícones: `WhiteSur-dark`.
   - Cursor: `WhiteSur-cursors`.
   - Sons do sistema: Pacote de efeitos sonoros do macOS instalado em `/usr/share/sounds/bigsur`.

---

## Como entrar no seu novo ambiente macOS

1. Faça **Logout** (Encerrar Sessão) no Pop!_OS.
2. Na tela de login, clique no seu usuário.
3. No canto inferior da tela (ou no ícone de engrenagem), selecione a sessão:
   - **Plasma (Wayland)** (Recomendado) ou **Plasma (X11)**.
4. Digite sua senha e entre. O desktop abrirá 100% transformado em macOS!
