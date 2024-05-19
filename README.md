# Visual Studio Code
## extensions.txt
Use o seguinte comando para ler o arquivo extensions.txt e instalar todas as extensões listadas:
</br>
<code>cat extensions.txt | xargs -n 1 code --install-extension</code>

### Autmomação com script
Para automatizar esse processo, você pode usar um script simples. Aqui está um exemplo de script ´install-extensions.sh´:
</br>
<code>
#!/bin/bash
# Script to install VS Code extensions from a list

if [ -f "extensions.txt" ]; then
    while read extension; do
        code --install-extension $extension
    done < extensions.txt
else
    echo "extensions.txt file not found!"
fi
</code>
</br>
Você pode clonar esse repositório e executar esse script:
<code>./install-extensions.sh</code>

## settings.json
Além das extensões, você pode querer salvar suas configurações. O VS Code armazena suas configurações em arquivos JSON. Você pode salvar o conteúdo da pasta .vscode ou especificamente o arquivo settings.json.
<code>cp ~/.config/Code/User/settings.json</code>
E depois, configurar um novo ambiente:
</br>
<code>cp settings.json ~/.config/Code/User/</code>

---------------------------------------
