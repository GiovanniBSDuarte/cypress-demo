FROM mcr.microsoft.com/devcontainers/javascript-node:18

# Instalar dependências para ambiente gráfico
RUN apt-get update && apt-get install -y \
    xfce4 \
    xfce4-goodies \
    x11vnc \
    xvfb \
    novnc \
    websockify \
    xterm \
    && apt-get clean

# Instalar Cypress
RUN npm install -g cypress

# Criar script para iniciar o desktop remoto
RUN echo '#!/bin/bash\n\
Xvfb :1 -screen 0 1280x800x24 &\n\
x11vnc -display :1 -nopw -forever -rfbport 5901 &\n\
websockify --web=/usr/share/novnc/ 6080 localhost:5901 &\n\
startxfce4 &' > /usr/bin/start-desktop && chmod +x /usr/bin/start-desktop

# Definir variáveis de ambiente para XFCE
ENV DISPLAY=:1
