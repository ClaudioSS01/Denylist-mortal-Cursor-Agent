# Cursor Agent — Denylist Mortal (README)

## Como usar no Cursor

1. **Cursor → Settings → Features → Command denylist**  
2. Copie cada comando abaixo (botão “Copy” do GitHub) e cole no painel.  
3. Salve.

> **Por quê?** Todos são comandos destrutivos: apagam disco, formatam partição, baixam código não-verificado ou matam processos críticos.

---

## Linux / macOS

| Comando | Por que é perigoso |
|---------|-------------------|
| ```rm -rf /``` | Apaga todo o sistema. |
| ```sudo rm -rf /*``` | Idem, mas como root. |
| ```mv ~ /dev/null``` | Remove todo seu home. |
| ```dd if=/dev/random of=/dev/sda``` | Sobrescreve o disco com lixo. |
| ```:(){ :|:& };:``` | Fork-bomb que trava o SO. |
| ```chmod -R 777 /``` | Remove segurança de permissões. |
| ```find / -type f -exec rm -f {} \;``` | Exclui todos os arquivos. |
| ```mkfs.*``` | Formata partições. |
| ```kill -9 1``` | Mata o init e derruba o sistema. |
| ```killall5``` | Encerra todos os processos. |
| ```> ~/.bash_history``` | Apaga rastros. |
| ```wget URL -O - \| bash``` | Executa código remoto não confiável. |
| ```curl URL \| bash``` | Idem. |
| ```echo MAL > /etc/passwd``` | Corrompe banco de usuários. |
| ```shutdown now``` | Desliga sem aviso. |
| ```reboot``` | Reinicia sem aviso. |

---

## Windows

| Comando | Por que é perigoso |
|---------|-------------------|
| ```format C: /Q /Y``` | Formata drive C:. |
| ```del /f /s /q C:\*``` | Apaga todos os arquivos. |
| ```rd /s /q C:\``` | Remove diretórios recursivamente. |
| ```takeown /R /F C:\``` | Toma posse de tudo (quebra ACL). |
| ```icacls C:\ /grant Everyone:F /T``` | Concede acesso total a todos. |
| ```cipher /w:C``` | Faz wipe do disco. |
| ```reg delete HKLM /f``` | Remove hive crítico do Registro. |
| ```reg delete HKCU /f``` | Apaga perfil do usuário. |
| ```reg delete HKCR\.exe /f``` | Quebra associação de executáveis. |
| ```assoc .exe=``` | Idem, via assoc. |
| ```powershell -NoProfile -ExecutionPolicy Bypass -Command "IEX (Invoke-WebRequest URL).Content"``` | Executa script remoto malicioso. |
| ```bitsadmin /transfer badjob URL C:\a.exe``` | Baixa malware usando BITS. |
| ```diskpart /s %TEMP%\wipe.txt``` | Automatiza diskpart para limpar discos. |
| ```taskkill /F /IM svchost.exe``` | Mata serviços essenciais. |
| ```shutdown -s -t 0``` | Desliga imediatamente. |
| ```shutdown -r -t 0``` | Reinicia imediatamente. |

---

