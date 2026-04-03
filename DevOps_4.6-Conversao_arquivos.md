## Conversão de arquivos

Temos uma ferramenta muito útil nesse processo: o comando convert. Esse comando nos permite converter, editar e exibir imagens em diversos formatos.

A sintaxe do comando é bem prática:

```
convert [opções] arquivo_entrada arquivo_saída
```

## Para converter uma imagem de .jpg para .png, podemos escrever a seguinte instrução:
```
convert imagem.jpg imagem.png
```

## E se quiséssemos redimensionar um conjunto de imagens .jpg para uma resolução padrão 800x600?

```
convert imagem.jpg -resize 800x600 imagem_redimensionada.jpg
```

## Crie um script que seja capaz de converter todos os arquivos com extensão .jpgde um diretório para .png de forma simples.

```
# Indicamos o interpretador
#!/bin/bash

# Solicitamos a indicação do caminho do diretório
read -p "Digite o caminho do diretório com as imagens JPG: " diretorio

# Verificamos se o diretório indicado existe
if [ ! -d "$diretorio" ]; then
    echo "Diretório não encontrado: $diretorio"
    exit 1
fi

# Convertemos todas as imagens JPG para PNG no diretório
for imagem_jpg in "$diretorio"/*.jpg; do
    convert "$imagem_jpg" "${imagem_jpg%.jpg}.png" && echo "Imagem convertida: ${imagem_jpg%.jpg}.png" || echo "Falha na conversão: $imagem_jpg"
done

echo "Conversão concluída!"
```

