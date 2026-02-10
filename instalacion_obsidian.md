# Instalación de Obsidian

# 1. En la pagina oficial se descarga un archivo : Obsidian-1.11.4.AppImage
se crea una carpeta llamada .apps/obsidian para guardar alli la imagen de Obsidian, y luego se dan los permisos de acceso sobre esta carpeta
```bash
mkdir -p "$HOME/.apps/Obsidian" && \
mv "$HOME/Descargas"/Obsidian-1.11.4.AppImage "$HOME/Applications/Obsidian/Obsidian.AppImage" && \
chmod +x "$HOME/.apps/Obsidian/Obsidian.AppImage"
```

---

# 2. Verificar ejecución:
```bash
"$HOME/Applications/Obsidian/Obsidian.AppImage"
```
si no funciona, ejecutar
```bash
"$HOME/Applications/Obsidian/Obsidian.AppImage" --no-sandbox
```

---

# 3. Se busca un icono representativo de Obsidian:
```bash
APP="$HOME/Applications/Obsidian/Obsidian.AppImage" && \
TMP="$(mktemp -d)" && \
cd "$TMP" && \
"$APP" --appimage-extract >/dev/null && \
ICON="$(find squashfs-root -type f \( -path '*/512x512/*' -o -path '*/256x256/*' -o -path '*/128x128/*' \) -iname '*obsidian*.png' | sort -r | head -n 1)" && \
[ -z "$ICON" ] && ICON="$(find squashfs-root -type f -iname '*obsidian*.png' | head -n 1)" && \
install -Dm644 "$ICON" "$HOME/.local/share/icons/obsidian.png" && \
cd "$HOME" && \
rm -rf "$TMP"
```

---

# 4. Creador del lanzador de obsidian
```bash
mkdir -p "$HOME/.local/share/applications" && \
cat > "$HOME/.local/share/applications/obsidian.desktop" <<EOF
[Desktop Entry]
Type=Application
Name=Obsidian
Comment=Obsidian
Exec=$HOME/Applications/Obsidian/Obsidian.AppImage --no-sandbox %U
Icon=$HOME/.local/share/icons/obsidian.png
Terminal=false
Categories=Office;Utility;TextEditor;
StartupWMClass=obsidian
EOF
```

---

# 5. Actualizar cache:
```bash
update-desktop-database "$HOME/.local/share/applications" >/dev/null 2>&1 || true
```

---

# 6. Crear acceso directo en escritorio (si se requiere):
```bash
DESK="$(xdg-user-dir DESKTOP)" && \
cp "$HOME/.local/share/applications/obsidian.desktop" "$DESK/Obsidian.desktop" && \
chmod +x "$DESK/Obsidian.desktop" && \
gio set "$DESK/Obsidian.desktop" metadata::trusted true 2>/dev/null || true
```