## Comando condicional `if` 
-> para avaliar uma condição e direcionar o próximo passo na execução do código. O trecho de código a seguir apresenta a sintaxe adotada no Bash:

```
if [ condição ]; then
  # Comandos a serem executados se a condição testada for verdadeira.
elif [ outra condição ]; then
  # Comandos a serem executados se a primeira condição testada for falsa e a segunda for verdadeira.
else
  # Comandos a serem executados se nenhuma das condições testadas for verdadeira.
fi
```

Repare que a sintaxe do comando possibilita o teste de várias condições, permitindo a execução de diferentes blocos de comandos com base nesses testes.

## Exemplos de operadores

Igualdade entre duas strings
```
if [ "$string1" = "$string2" ]; then
```

# Comandos a serem executados se as strings forem iguais.

Desigualdade entre duas strings
```
if [ "$string1" != "$string2" ]; then
```
  # Comandos a serem executados se as strings forem distintas.

Igualdade entre dois números
```
if [ "$numero1" -eq "$numero2" ]; then
```
  # Comandos a serem executados se os números forem iguais.
fi
Desigualdade entre dois números
```
if [ "$numero1" -ne "$numero2" ]; then
```
  # Comandos a serem executados se os números forem distintos.


Número maior que outro
```
if [ "$numero1" -gt "$numero2" ]; then
```
  # Comandos se o primeiro número for maior que o segundo.

Número menor que outro
```
if [ "$numero1" -lt "$numero2" ]; then
```
# Comandos se o primeiro número for menor que o segundo.

Número maior ou igual a outro
```
if [ "$numero1" -ge "$numero2" ]; then
```
  # Comandos se o primeiro número for maior ou igual ao segundo.

Verificar existência de arquivo ou diretório
```
if [ -e "/caminho/do/arquivo" ]; then
```
  # Comandos caso o arquivo ou diretório exista.
