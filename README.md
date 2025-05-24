<h1>Cursor Agent — Denylist Mortal</h1>
<p>
<strong>Passos:</strong><br>
1. <em>Cursor → Settings → Features → Command denylist</em><br>
2. Clique <kbd>Copiar</kbd> em cada linha abaixo e cole no painel.<br>
3. Salve.
</p>

> Todos os comandos abaixo são destrutivos (apagão de disco, formatação, download de malware, etc.).

<hr/>

<style>
table{border-collapse:collapse;width:100%;max-width:960px;}
th,td{border:1px solid #ddd;padding:6px;}
th{background:#fafafa;text-align:left;}
input{width:100%;font-family:monospace;border:none;background:#f5f5f5;}
button{padding:4px 10px;margin-left:4px;cursor:pointer;}
small{color:#666;}
</style>
<script>
function cp(btn){navigator.clipboard.writeText(btn.previousElementSibling.value);}
</script>

## Linux / macOS
<table>
<thead><tr><th>Comando</th><th>Perigo</th></tr></thead>
<tbody>
<tr><td><input value="rm -rf /" readonly><button onclick="cp(this)">Copiar</button></td><td>Apaga todo o sistema.</td></tr>
<tr><td><input value="sudo rm -rf /*" readonly><button onclick="cp(this)">Copiar</button></td><td>Idem, mas como root.</td></tr>
<tr><td><input value="mv ~ /dev/null" readonly><button onclick="cp(this)">Copiar</button></td><td>Remove todo seu home.</td></tr>
<tr><td><input value="dd if=/dev/random of=/dev/sda" readonly><button onclick="cp(this)">Copiar</button></td><td>Sobrescreve disco com lixo.</td></tr>
<tr><td><input value=":(){ :|:& };:" readonly><button onclick="cp(this)">Copiar</button></td><td>Fork-bomb que trava o SO.</td></tr>
<tr><td><input value="chmod -R 777 /" readonly><button onclick="cp(this)">Copiar</button></td><td>Remove segurança de permissões.</td></tr>
<tr><td><input value="find / -type f -exec rm -f {} \\;" readonly><button onclick="cp(this)">Copiar</button></td><td>Exclui todos os arquivos.</td></tr>
<tr><td><input value="mkfs.*" readonly><button onclick="cp(this)">Copiar</button></td><td>Formata partições.</td></tr>
<tr><td><input value="kill -9 1" readonly><button onclick="cp(this)">Copiar</button></td><td>Mata init → crash.</td></tr>
<tr><td><input value="killall5" readonly><button onclick="cp(this)">Copiar</button></td><td>Encerra processos críticos.</td></tr>
<tr><td><input value="> ~/.bash_history" readonly><button onclick="cp(this)">Copiar</button></td><td>Apaga rastros.</td></tr>
<tr><td><input value="wget URL -O - | bash" readonly><button onclick="cp(this)">Copiar</button></td><td>Executa código remoto.</td></tr>
<tr><td><input value="curl URL | bash" readonly><button onclick="cp(this)">Copiar</button></td><td>Idem.</td></tr>
<tr><td><input value="echo MAL > /etc/passwd" readonly><button onclick="cp(this)">Copiar</button></td><td>Corrompe usuários.</td></tr>
<tr><td><input value="shutdown now" readonly><button onclick="cp(this)">Copiar</button></td><td>Desliga sem aviso.</td></tr>
<tr><td><input value="reboot" readonly><button onclick="cp(this)">Copiar</button></td><td>Reinicia sem aviso.</td></tr>
</tbody>
</table>

## Windows
<table>
<thead><tr><th>Comando</th><th>Perigo</th></tr></thead>
<tbody>
<tr><td><input value="format C: /Q /Y" readonly><button onclick="cp(this)">Copiar</button></td><td>Formata drive C:.</td></tr>
<tr><td><input value="del /f /s /q C:\\*" readonly><button onclick="cp(this)">Copiar</button></td><td>Apaga todos os arquivos.</td></tr>
<tr><td><input value="rd /s /q C:\\" readonly><button onclick="cp(this)">Copiar</button></td><td>Remove diretórios raiz.</td></tr>
<tr><td><input value="takeown /R /F C:\\" readonly><button onclick="cp(this)">Copiar</button></td><td>Quebra ACLs.</td></tr>
<tr><td><input value="icacls C:\\ /grant Everyone:F /T" readonly><button onclick="cp(this)">Copiar</button></td><td>Permissão total a todos.</td></tr>
<tr><td><input value="cipher /w:C" readonly><button onclick="cp(this)">Copiar</button></td><td>Wipe de disco.</td></tr>
<tr><td><input value="reg delete HKLM /f" readonly><button onclick="cp(this)">Copiar</button></td><td>Remove hive crítico.</td></tr>
<tr><td><input value="reg delete HKCU /f" readonly><button onclick="cp(this)">Copiar</button></td><td>Apaga perfil usuário.</td></tr>
<tr><td><input value="reg delete HKCR\\.exe /f" readonly><button onclick="cp(this)">Copiar</button></td><td>Quebra .exe.</td></tr>
<tr><td><input value="assoc .exe=" readonly><button onclick="cp(this)">Copiar</button></td><td>Desassocia executáveis.</td></tr>
<tr><td><input value='powershell -NoProfile -ExecutionPolicy Bypass -Command "IEX (Invoke-WebRequest URL).Content"' readonly><button onclick="cp(this)">Copiar</button></td><td>Baixa/roda script malicioso.</td></tr>
<tr><td><input value="bitsadmin /transfer badjob URL C:\\a.exe" readonly><button onclick="cp(this)">Copiar</button></td><td>Download furtivo via BITS.</td></tr>
<tr><td><input value="diskpart /s %TEMP%\\wipe.txt" readonly><button onclick="cp(this)">Copiar</button></td><td>Diskpart wiping.</td></tr>
<tr><td><input value="taskkill /F /IM svchost.exe" readonly><button onclick="cp(this)">Copiar</button></td><td>Mata serviços essenciais.</td></tr>
<tr><td><input value="shutdown -s -t 0" readonly><button onclick="cp(this)">Copiar</button></td><td>Desliga imediato.</td></tr>
<tr><td><input value="shutdown -r -t 0" readonly><button onclick="cp(this)">Copiar</button></td><td>Reinicia imediato.</td></tr>
</tbody>
</table>

<hr/>
<small>GitHub desativa JavaScript em Markdown renderizado. Abra este arquivo localmente ou publique via GitHub Pages para ativar os botões.</small>
