============================== Módulo 1 ==================================

--------------------------- Tipos de dados -------------------------------

- Tipos Primitivos

Os primitivos sao imutáveis, ou seja, ao longo do tempo seu valor nao é 
alterado.

Sao eles:
    
    -number
        Sao formatos de números

    -string
        Sao formatos de textos

    -boolean
        Sao formatos booleanos

    -symbol
        Sao formatos de simbolos

    -object
        Sao formatos de determinado conteudo com suas caractesteriscas.

    -undefined
        Sei la


Como saber qual o tipo de dado está sendo trabalhado?

Basta utilizar a funçao "typeOf"

ex:

let number = 10

typeOf number 
> number




--------------------------- Number -------------------------------


O tipo number é primitovo, imutável e é representado internamente
pelo padrao IEEE754 de 64 bits.

O JS suporta 4 sistemas de númeraçao:

-decimal
    Conhecido pela base 10, deve-se iniciar com nuémro de 1 a 9, 
    seguido por números de 0 a 9 com ou sem ponto, indicando se é 
    inteiro ou decimal

-hexadecimal
    COnhecido pela base 16, deve ser iniciado por 0x ou 0X, seguido
    por números de 0 a 9 e letras de A a F

-binário
    Conhecido pela base 2, deve ser iniciado com 0b ou 0B, seguido
    por nuḿeros de 0 a 1. Se le sempre da direita para esquerda, 
    elevando na base 2

-octal
    Conhecido pela base 9, deve iniciar com 0, 0o ou 0O seguido por 
    números de 0 a 7

Exemplos de Numbers na imagem de título NUMBERS.

Algumas funçoes para se trabalhar com numbers:

number = 123.4

-toExponential()
    Faz com que se movam casas decimais à esquerda:

    (number).toExponential(10)
    > 1.2340000000e+2

-toFixed()
    Limita quantas casas decimais devem ser exibidas de um número.

    (number).toFixed(10)
    > 123.40000000





--------------------------- Conversao Numerica -------------------------------

    A funçao mais comum para isso é a funçao "Number()"

    Podemos utiliza-la passando strings e números binários

    Ex:

    Number("10") = 10

    Number("9.9") = 9.9

    Number("0xFF") = 255

    Number("0b10") = 2

    Number("0o10") = 8

    Number() = 0

    Number("Javascript") = NaN

    Também é possível fazer isso com operadores números, porém nao é o recomendado.

    Ex:

    ~~"10" = 10

    +"10" = 10

    "10"-0 = 10

    "10"*1 = 10

    "10"/1 = 10

    CUIDADO:

    "10" + 0 = "100"
        
        O operador +, pode encarar a operaçao como concatenaçao.


Conversáo para String

    A funcáo mais comum para isso é a "toString()"

    Ex:

    (0xA).stoString(10) = '10'

    (0b1010).stoString(16) = 'a'

    (010).toString(2) = '1000'

    (10).toString(8) = '12'


Conversao para numeros inteiros

    A funcao utilizada é a "parseInt()"

    parseInt("10", 10) = 10  (base decimal)

    parseInt("9.9", 10) = 9

    parseInt("A", 16) = 10

    parseInt("11", 2) = 3

    parseInt("010", 8) = 8


Conversao para numeros flutuantes

    A funcao utilizada é "parseFloat()"

    parseFloat("10") = 10

    parseFloat("2.5") = 2.5

    parseFloat("0xFF") = 0 (A funcao retornar todos os numeros antes das letras)

    parseFloat("0b10") = 0  x-----------x-----------x---------x---------x-----x




--------------------------- IEEE 754 -------------------------------


Os numeros sao representados através do padrao IEEE 754, e essa padronizacao
reflete dirente em alguns calculos de arredondamentos, onde a soma de numeros
flutuantes podem gerar discordancia em seu resultado. 

Mantenha-se atento a isso no JS.





--------------------------- math API -------------------------------


Math é um objeto gloval que contém constasntes metematática e métodos
para a realizaçao de operaçoes envolvendo nuḿeros

- Constantes:

    E___________E
    LN10________logaritmo natural de 10
    LN2_________logaritmo natural de 2
    LOG10E______logaritmo de E na base 10
    LOG2E_______logaritimo de E na base 2
    PI__________PI
    SQRT1_2_____Raiz quadrada de 1/2
    SQRT________Raiz quadrada de 2

Exemplos:

Math.E
>2.718281828459045

Math.LN10
>2.30259509294046

Math.LN2
>0.6931471805599453

etc...

-Operaçoes com Math basicas:

    abs_______Converte osinal de um número para positivo
    ceil______Arredonda o número para cima
    floor_____Arredonda o número para baixo
    round_____Arredondo o número para cima se o deciaml for de 5 a 9 e para baixo
    se for de 1 a 4
    sign______retona 1 se o número for positivo e -1 se for negativo
    trunc_____elimina a parte decimal do número, tornando-o um inteiro
    min_______retorna o menor numero de um array
    max_______retorna o maior numero de um array
    random____retorna um numero aleatorio dentro do parametro informado

Exemplos:

    Math.abs(10)
    >-10

    Math.ceil(1.1)
    >2
     
    etc...



--------------------------- Template Literals -------------------------------


Adcionados no ecma6, é possível realizar interpolações, quebras de linhas, e outras
facilidades apenas se utlizando da cráse, ao invés das aspas duplas ou simples.

Ex:

let carro = "celta"

console.log(`O meu carro é um ${carro}.`)
> O meu carro é um celta.

Let dias = `segunda
terça 
quarta
quinta
sexta
sábado
domingo`

console.log('dias')
>segunda
terça
quarta
quinta
sexta
sábado
domingo



--------------------------- Strings APIs -------------------------------


Semelhantes as Math APIs, as Strings APIS servem como metodos para manipular
e trabalhar com strings e vetores.

São eles: 

- lenght:
    
    Retorna o tamanho da string (iniciando em 0)

- indexOf:

    Retorna a primeira posição do carácter passado como parâmetro.
    Ex:

    const carro = "celta"
    carro.indexOf(l)
    >2

-lastIndexOf:
    
    Retorna a ultima posiçao do carácter passado como parâmetro.

-toUpperCase:

    Retorna uma nova string convertendo todos os carácteres para maiúsculo.

-toLowerCase:

    Retorna uma nova string convertendo todos os carácteres para minúsculo.

-charAt:

    Retorna o carácter na posição passada como parâmetro.
    Ex:
    const computador = 'laptop'
    computador.charAt(1)
    >a

-charCodeAt:

    Retorna um código referete ao carácter na posição passada por parâmetro. 
    Ex:
    const computador = 'laptop'
    computador.charCodeAt(1)
    >97  (código que representa a letra "a")

-fromCharCode:

    Retorna um carácter com base no código passado por parâmetro. (Acontece
    o inverso de charCodeAt)
    Ex:
    String.fromCharCode(97)
    >a

-includes:

    Retorna verdadeiro se uma String contém a String passada por parâmetro
    Ex:
    const linguagem = 'javascript'
    linguagem.includes('java')
    >true

-startWith:

    Retorna verdadeiro se a String inicia com a String passada por parâmetro
    Ex:
    const linguagem = 'python'
    linguagem.startWith("p")
    >true

-endsWith

    Retorna verdadeiro se a String termina com a String passada por parâmetro.
    Ex:
    conste lingaugem = 'java'
    linguagem.endsWith = 'a'
    >true

-localeCompare

    Compara a extensão de uma string passada, entre outra declarada.
    1 = String menor
    0 = String de mesmo tamanho
   -1 = String maior

    Ex:
    const nome = 'caio'
    caio.localeCompare('montenegro')
    >-1

    Obs: Se for realizada uma comparação entre duas letras, será considerado o
    código número da letra.

-match (somente para expressões regulares)

    Retorna partes da String com base na RegEXP passada por parâmetro.
    Ex:

    const linguagem = 'javascript'
    linguagem.match(/a/g) (estou procurando o caractér A, o G faz com que todos os As sejam retornados)
    >['a', 'a']

    linaguagem.atch(/a/)
    >['a', index: 1, input: 'javascript']


-search (somente para expressões regulares)

    Retorna a primeira posição encontrada com base na RegExp passada por parâmetro (similar a indexOF)
    Ex:

    const carro = 'celta'
    carro.search(/l/)
    >2

-Replace

    retorna uma nova String resultada da substituição da String ou RegExp passada no
    primeiro parâmetro pelo segundo parâmetro.
    Ex:

    const linguagem = 'Javascript'
    linguagem.replace('Java', 'Ecma')
    >'Ecmascript'

    linguagem.replace(/a/g, 4)
    >J4v4script

-Slice

    Retorna parte da string ou array, dentro do intervalo passado como parâmetro:
    Ex:

    const carro = 'celta'
    carro.slice(1, 3)
    >'el'

    carro.slice(0, -1)
    >'celt'

    carro.slice(-1)
    >'a'

-Split

    Retorna um array contendo  resultado da divisãoda sString original de acordo com o critério passado por parâmetro
    Ex:

    const carro = 'celta'
    const casa = 'sobrado'
    const linguagem = 'javascript'
    carro;casa;linguagem.split(';')
    >['celta', 'sobrado', 'javascript']



-Substring:

    Similar ao slice, porém não aceita valores negativos como parâmetros e permite a inversão dos
    parâmetros.
    Ex:

    const linguagem = 'javascript'
    linguagem.substring(4, 0)
    >'Java'  
    (necessáriamente o segundo parâmetro deve ser maior que o primeiro, do contrário será
    invertido automaticmanente pelo JS)

    linguagem.substring(4)
    >'script'

-concat:

    Irá realizar a concatenaçao da string invocada, com a string passada como parâmetro.
    Ex:
    
    const linguagem = 'Java'
    linguagem.concat('script')
    >'Javascript'

-padStart:

    Completa a string com um número carácteres passadas como parâmetro, e qual carácter
    deverá ser usado para completar.
    Ex:

    const placa = '123
    placa.padStart(6, 'H')
    >HHH123'

-padEnd:

    Similar a padstart, mas completará com carácteres no final.
    Ex:

    const placa = 'HHH'
    placa.padEnd(6, 1)
    >'HHH111'

-repeat:

    Repete um carácter:
    ex:

    const carro = 'celta'
    const cor = 'preto'

    cor.trim(2)
    >'pretopreto'

    carro.concat(cor.trim(2)
    >'celtrapretopreto'

-trim:

    Eliminará todos os espaços em brando da string.
    Ex:

    const desejo = 'Ficar Rico'
    desejo.trim()
    >'FicarRico'

-trimLeft

    Elminará todos espaços em branco no início.
    Ex:

    const desejo = '   aumento'
    desejo.trimLeft()
    >'aumento'

-trimRight

    Elimina espaços em branco no fim.
    Ex:

    const desejo = 'riqueza    '
    desejo.trimRight()
    >'riqueza'


--------------------------- Boleanos -------------------------------


O tipo Boolean é primitivo, imutável e representado pelas palavras reservadas "True" e "False"

Qualquer valor atribuído a uma variável que nao sejam os seguintes:

    - NaN
    - 0
    - '' (string vazia)
    - false
    - Undefined
    - null

O restantes é 'True'



---------------------- Operadores Boleanos ------------------------


Operadores de comparação são:

 - ==
    Representa igualdade de valores

 - ===
    Representa igualdade de valores e typeOf

 - != 
    Representa diferença entre valores

 - !===
    Representa diferença entre valores e typeOf

 - <
    Representa valore menor 

 - >
    Representa valor maior

 - <=
    Representa valor menor igual 

 - >=
    Representa valor maior igual


Operadores Lógicos:

 - ||
    Representa alternativa entre valores (ou)

 - &&
    Representa duas situações ( e )


Operador ternário

 - ?

 Simplifica a escrita de condicionais que contém apenas uma
 condição. 
 Ex:

 (expressao) ? 'return para true' : 'return para false'




 --------------------------- Symbol -------------------------------

 
 'É mais um tipo primitivo, que atua como uma chave única em um 
 objeto'



 --------------------------- Expressões Regulares -------------------


 As expressões regulares sao estreuturas formadas por uma sequência de carácteres
que especificam um padrão formal que servem para validar, extrair ou meesmo
substituir caracteres dentro de uma String.


A escrita é feita dentro de duas baras / / 


------------------------------- Objetos -------------------------------


Um objeto é uma coleção dinânima de propriedades definidas por chaves, que 
podem ser do tipo String ou Symbol, e valores que podem ser de qualquer tipo de
dado.

Formas de criar um objeto:

    - Notação literal
        A mais usual de todas, basta digitar {}.
        Ex:

        const livro = {cor: "azul"}

        Short hand:
            É possível imputar variáveis como valores para as chaves, e caso
            as variáveis tenham o mesmo nome da chave, é possível deixar 
            apenas o nome da chave dentro do objeto:

            const cor = 'azul'

            const livro = {
                cor
            }

        Obs: 
            Em caso de um nome da chave for complexo, como por exemplo:
            cor-principal. É necessário colocar o nome da chave entre aspas.

            Também é possível atribuir o nome das chaves em tempo de execução,
            isso é, durante a execução do programa:

                const key1 = 'title'

                const book = {
                    [key1] = 'Clean Code'
                }
                console.log(book)
                >{title: 'Clean Code'}

            Atribuindo valores por veio de referência:
                const book = {}
                book.title = 'Clean Code'
                book.color = 'blue'

                console.log(book)
                >{title: 'Clean Code', color: 'blue'}

                ou 

                const key1 = 'Title'
                const book = {}

                book[key1] = 'Clean Code'
                console.log(book)
                >{title: 'Clean Code'}

            As propriedades das chaves, podem ser consultadas da mesma forma

                const book = {
                    title: 'Clean Code'
                    color: 'blue'
                }

                console.log(book.title)
                >'Clean Code'

    - Função construtora (new)
        Existe uma função para criar os objetos, ela é chamada de new. 
        Ex:

        new Object()
        >{}

    - Método Create da Object API
        Terceira fora é através da Object API.
        Ex:

        Object.create(null)
        >{}


------------------------------- Undefined e Null -------------------------------


O tipo "Undefined" é retornado caso a chave não seja encontrada.
Exemplo:

    const book = {
        title: "Clean Code",
        color: "Blue"
    }
    console.log(book.publisher)
    >Undefined

Qual a diferença entre null e undefined?
    Null singnifica ausencia de valor, enquanto undefined significa que a propriedade
    sequer existe.

    Para verificar se a propriedade existe, podemos utilizar o operador "In".
    Ex:

    console.log("title" in book)
    >true

Porém jamais defina uma propriedade como Undefined ou Null caso deseje apaga-la.
Para isso use o operador "Delete".

    delete book.title
    console.log("title" in book) 
    >false



------------------------------- Comparando Objetos -------------------------------


A comparação dos objetos é feita por meio da sua referêrencia (nome), assim, ainda que dois 
objetos tenham exatamente as mesmas propriedades eles serão considerados diferentes.
Ex:

    const book1 = {
        title: 'Clean Code',
        author: 'Robert C. Martin'
    }


    const book2 = {
        title: 'Clean Code',
        author: 'Robert C. Martin'
    }

    console.log(book1 == book2)
    >false

    console.log(book1 === book2)
    >false

    console.log(book1 === book1)
    >True

Uma das formas para comparar os objetos é analisando cada uma das suas proriedades por meio da
comparação das chaves e valores. Podemos usar uma biblioteca, ou simplesmente criar um 
algoritmo de comparação.
Ex:

    let equal = true

    for (let key in book1) {
        if (book1[key] !== book2[key]) equal = false
    }

    obs: É necessário criar o mesmo laço para o book2, pois o parâmetro está somente
    para o book1, e caso o book2 tenha mais parâmetros, a const "equal" permanecerá
    True.

    for (let key in book2) {
        if (book1[key] !== book2[key]) equal = false
    }

    console.log(equal)
    >true

Essa análise pode ser considerada superficial, já que uma comparação eficiente, deve analisar
os protótipos do objeto.



-------------------------------------- Herança ----------------------------------------

A herença é o compartilhamento de proriedades entre objetos, e tem como bojetivo permitir
o reuso de código, evitando duplicações.

No Javascript, a herança se da entre objetos e não entre classes como em outras linguagens.
Também conhecida como herança baseda em protótipos.
Ex:

    const scheme = {
        name: "Scheme", 
        year: 1975,
        paradigm: "Functional"
    }

    const javascript = {
        name: "Javascript",
        year: 1995, 
        paradigm: "Functional"
    }   

    Repare que ambos os objetos tem a mesma propriedade paradgm como "Functional". Neste
    caso, para usarmos a herança e evitar esssa duplicidade, criaremos um novo Objeto:

    const functionalLanguage = {
        paradigm: "Functional" 
    }

- Metodo __Proto__
    A propriedade __proto__ é uma referência para o protótipo do objeto. Sendo assim, 
    iremos substituir a propriedade paradigm, dos objetos que herdaram a propriedade:

    
    const scheme = {
        name: "Scheme", 
        year: 1975,
        __proto__: functionalLanguage
    }

    const javascript = {
        name: "Javascript",
        year: 1995, 
        __proto__: functionalLanguage
    }

    Obs: Atente-se para consulta do objeto que herda propriedades, pois para minimizar
    o processamento, nao serão exibidas as propriedades herdadas, isso porquê a propriedade
    está de fato no objeto que fornece a herança... Sendo assim a consulta só irá exibir o 
    a propriedade herdada, caso seja feita uma consulta direta a referência da propriedade.
    Ex:

        console.log(scheme)
        >{name: "Scheme", year: 1975}

        console.log(scheme.paradigm)
        >Functional
    

- HasownProperty
    Este método pode ser utilizado para determinar se uma proriedade pertence ao objeto.
    Ex:

        for(let key in scheme) {
            console.log(key, scheme.hasOwnProperty(key))
        }
        >name true
        >year true
        >paradigm false 


- Object.setPrototypeOf 
Além de __Proto__ também é possível utilizar o Object.setPrototypeOf para setar uma 
herança e object.getPrototypeOf para consultar a propriedade. Ambos permitem a 
interação com o protótpipo do objeto.
Ex:

    Object.setPrototypeOf(scheme, functionalLanguage)
    conste javascript = {
        name: "Javascript"
        year: 1995
    }

    Object.setprototypeOf(javascript, functionallanguage)

    for (let key in scheme) {
        console.log(key, scheme.hasOwnProperty(key))
    }
    >name true
    >year true
    >paradigm false


-Object.create
 Com este método é possível criar um objeto passando o seu protótipo por parâmetro
 Ex:
    
    const functional = {
        paradigm : "Functional"
    }

    conste scheme = Object.create(functional)
    scheme.name = "Scheme"
    scheme.year = 1975

    
Obs: Caso a mesma propriedade exista no objeto e no seu protótipo, a proriedade 
do próprio objeto é retonada, fazendo sombra à proriedade do protótipo.