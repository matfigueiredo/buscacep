# Busca de CEP em Go

Esse projeto tem como objetivo criar um servidor local em Go que possa receber requisições GET contendo um CEP como query string e retornar um JSON com os dados referentes a esse CEP.

### Pré requisitos
Antes de começar, certifique-se que você tenha os seguintes pré-requisitos instalados em sua máquina:
* Go (versão 1.16 ou superior)
* Git

### Instalação e execução
1. Faça o clone deste repositório em sua máquina: 
`git clone https://github.com/matfigueiredo/buscacep`
2. Acesse o diretório do projeto
3. Execute o comando abaixo para baixar as dependências do projeto:
`go mod download`
4. Execute o servidor local com o comando abaixo:
`go run main.go`
5. O servidor estará rodando em `http://localhost:8080`. Você pode acessar essa URL em seu navegador ou utilizar um cliente HTTP para fazer requisições GET.

### Utilização
Para fazer a busca de um CEP, faça uma requisição GET para a URL http://localhost:8080/cep?{CEP desejado}.

Por exemplo, se você deseja buscar o CEP 01234567, faça a seguinte requisição GET:
`curl http://localhost:8080/cep?01234567`

O servidor retornará um JSON com os dados referentes ao CEP buscado:
~~~json
{
    "cep": "01234567",
    "logradouro": "Rua Exemplo",
    "complemento": "",
    "bairro": "Bairro Exemplo",
    "localidade": "São Paulo",
    "uf": "SP",
    "ibge": "3550308",
    "gia": "",
    "ddd": "11",
    "siafi": "7107"
}
~~~

### Considerações finais
Esse projeto é apenas um exemplo de como é possível criar um servidor em Go para realizar a busca de CEPs.
