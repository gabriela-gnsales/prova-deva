# Arquivos de marcação

### XML
##### eXtensible Markup Language → linguagem de marcação extensível

A linguagem de marcação XML surgiu em meados da década de 90, com o objetivo de estruturar documentos facilmente legíveis tanto para humanos quanto para máquinas.

Foi utilizado, principalmente, na década de 90/2000 para realizar a comunicação entre sistemas.

É constituído de tags, elementos que contém basicamente um nome e seu valor, sendo que um elemento pode conter, ao invés de um valor em texto, outros elementos recursivamente.

Como desvantagens, caracteriza-se por ser muito grande/extensível, o que torna complexa sua escrita e leitura, além de dificultar a absorção do conteúdo. Por esses motivos caiu em desuso, sendo substituído por outras linguagens de marcação.

* __Extensão:__ `.xml`
* __Exemplo sintaxe:__
```
<meu-elemento>
    <elemento-filho-1>
        <outro-elemento>
            <mais-um-elemento>
                valor
            </mais-um-elemento>
        </outro-elemento>
    </elemento-filho-1>
    <elemento-filho-2>
        valor do filho 2
    </elemento-filho-2>
</meu-elemento>
```

### JSON
##### JavaScript Object Notations → notação de objetos JavaScript

A especificação JSON surgiu por volta do ano 2000, mas só passou a fazer parte da linguagem JavaScript após o lançamento da versão 5 do ECMAScript. 

O formato JSON é utilizado para estruturar dados em formato de texto e permitir a troca de dados entre aplicações de forma simples, leve e rápida.

Esses arquivos utilizam do modelo "chave-valor", onde os elementos possuem um atributo que os identifica e que garante fácil acesso a cada um deles.

Atualmente, esse formato é suportado por diversos tipos de linguagem de programação, além de ser uma alternativa mais leve que o modelo XML. É utilizado, principalmente, para padrão da web de comunicação e criação de IaC (Infrastructure as Code).

* __Extensão:__ `.json`
* __Exemplo sintaxe:__
```
{
  "nome": "Maria José",
  "idade": 30,
  "salario": 15000.00,
  "tecnologias": [
    "HTML",
    "CSS",
    "JavaScript",
    "Python"
  ]
}
```

### YML
##### YAML Ain't Markup Language → YAML não é uma linguagem de marcação

YAML (pronuncia-se "iâmel") é um formato de marcação criado em 2001 mas que teve sua primeira versão em 2004. 

A linguagem possui diversas funcionalidades, implementando, assim como o JSON, um modelo "chave-valor", com elementos possuindo um identificador e seu devido valor, podendo ser de diversos tipos (como strings, números ou listas).

É utilizado, principalmente, para padronização de arquivos e criação de recursos via IaC (terraform, cloudformation, kubernetes...). Porém, não é usual na comunicação entre serviços, embora seja usado na elaboração do contrato, mas para enviar e receber informações é raro (JSON é usado nesse caso).

* __Extensões:__ `.yaml` (recomendada oficialmente) ou `.yml`
* __Exemplo sintaxe:__
```
exemplo1: meu valor sem aspas
exemplo2: "meu valor em aspas duplas"
exemplo3: 'meu valor em aspas simples'
exemplo4: |-
  Minha string dividida em várias
  linhas diferentes, com as quebras
  de linha sendo levadas em consideração
exemplo5: >-
  Outra string dividida em várias
  linhas, mas a diferença é que
  esta sintaxe ignora as quebras
  de linha
inteiro: 12
flutuante: 127.57
exponencial: 8.7e+4
exponencial2: 1.2e-4
hexadecimal: 0xFF
octal: 012 # a versão 1.2 do YAML só aceita octais como 0o12 e não mais 012
lista1:
  - valor1
  - valor2
  - valor3
lista2: [valor1, valor2, valor3]
pessoas:
  - nome: José Silva
    idade: 40
  -
    nome: Maria José
    idade: 35
# Comentários podem ocupar toda uma linha
nome: José # Ou estarem ao final de uma
```
