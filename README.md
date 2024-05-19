# Visual Studio Code
## extensions.txt
Use o seguinte comando para ler o arquivo extensions.txt e instalar todas as extensões listadas:
´cat extensions.txt | xargs -n 1 code --install-extension´

### Autmomação com script
Para automatizar esse processo, você pode usar um script simples. Aqui está um exemplo de script ´install-extensions.sh´:
`
#!/bin/bash
# Script to install VS Code extensions from a list

if [ -f "extensions.txt" ]; then
    while read extension; do
        code --install-extension $extension
    done < extensions.txt
else
    echo "extensions.txt file not found!"
fi
`
Você pode clonar esse repositório e executar esse script:
`./install-extensions.sh`

## settings.json
Além das extensões, você pode querer salvar suas configurações. O VS Code armazena suas configurações em arquivos JSON. Você pode salvar o conteúdo da pasta .vscode ou especificamente o arquivo settings.json.
´cp ~/.config/Code/User/settings.json´
E depois, configurar um novo ambiente:
´cp settings.json ~/.config/Code/User/´

===========================
