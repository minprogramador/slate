---
title: API Referencia

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - php

toc_footers:
  - <a href='#'>github.link</a>

includes:
  - errors

search: true
---

# Introduçāo

Bem vindo à API do Kittn! Você pode usar nossa API para acessar pontos de extremidade da API do Kittn, que podem obter informações sobre vários gatos, gatinhos e raças em nosso banco de dados.

Nós temos ligações de linguagem no Shell, Ruby, Python e JavaScript! Você pode visualizar exemplos de código na área escura à direita e pode alternar a linguagem de programação dos exemplos com as guias no canto superior direito.

Este exemplo de página de documentação da API foi criado com [Slate](https://github.com/lord/slate). Sinta-se à vontade para editá-lo e usá-lo como base para a documentação de sua própria API.

# Autenticação

> Para autorizar, use este código:

```shell
# Com shell, você pode apenas passar o cabeçalho correto com cada solicitação
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

> Certifique-se de substituir `meowmeowmeow` pela sua chave de API.


Kittn usa chaves de API para permitir o acesso à API. Você pode registrar uma nova chave de API Kittn em nosso [developer portal](http://example.com/developers).

O Kittn espera que a chave da API seja incluída em todas as solicitações da API para o servidor em um cabeçalho que se pareça com o seguinte:

`Authorization: meowmeowmeow`

<aside class="notice">
Você deve substituir <code>meowmeowmeow</code> com sua chave de API pessoal.
</aside>

# Gatinhos

## Obter todos os gatinhos

```shell
curl "http://example.com/api/kittens"
  -H "Authorization: meowmeowmeow"
```

> O comando acima retorna JSON estruturado assim:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

Este endpoint recupera todos os gatinhos.

### HTTP Request

`GET http://example.com/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | Se definido como true, o resultado também incluirá gatos.
available | true | Se definido como falso, o resultado incluirá os gatinhos que já foram adotados.

<aside class="success">
Lembre-se - um gatinho feliz é um gatinho autenticado!
</aside>

## Obter um gatinho específico

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

> O comando acima retorna JSON estruturado assim:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

Este endpoint recupera um gatinho específico.

<aside class="warning">Dentro de blocos de código HTML como este, você não pode usar o Markdown, então use <code>&lt;code&gt;</code> blocos para denotar o código.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | O ID do gatinho para recuperar

## Excluir um gatinho específico

```shell
curl "http://example.com/api/kittens/2"
  -X DELETE
  -H "Authorization: meowmeowmeow"
```

> O comando acima retorna JSON estruturado assim:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

Este endpoint exclui um gatinho específico.

### HTTP Request

`DELETE http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | O ID do gatinho para deletar

