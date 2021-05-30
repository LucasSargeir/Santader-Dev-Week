# Santader Dev Week - Backend

O Santander Dev Week é um evento de tecnologia que tem como objetivo compatilhar conhecimento das tecnologias utilizadas pela empresa nos seus projetos.



## Utilização

Embora criada para servir ao _frontend_ você pode utilizar a API fazendo suas requisições ao host: http://santander-dev-week-sargeiro.herokuapp.com/bootcamp/

Para mais informações e testes acesse a [página](http://santander-dev-week-sargeiro.herokuapp.com/bootcamp/swagger-ui.html).



## Backend

O _backend_ da aplicação foi feito em Java utilizando o _framework_ Spring. O objetivo desse parte do sistema foi montar uma API REST para que pudesse servir os dados para o [_frontend_](https://github.com/LucasSargeir/Santader-Dev-Week-Frontend).



**Dependencias**

- Spring
  - web
  - validation
  - data-jpa
- OpenAPI (Swagger)
- Postgresql



### Rotas



**Rota:** <span style="color:blue">GET</span> `/stock` 

**Corpo:**  nenhum

**Exemplo de Resposta:**

```json
[
  {
    "id": 0,
    "name": "string",
    "price": 0,
    "date": "2021-05-29",
    "variation": 0
  }
]
```





**Rota:** <span style="color:blue">GET</span> `/stock/{id}` 

**Corpo:** nenhum

**Exemplo de Resposta:**

```json
{
  "id": 0,
  "name": "string",
  "price": 0,
  "date": "2021-05-29",
  "variation": 0
}
```





**Rota:** <span style="color:green">POST</span> `/stock` 

**Corpo:**

```json
{
  "id": null,
  "name": "string",
  "price": 0,
  "date": "dd/MM/yyyy",
  "variation": 0
}
```

**Exemplo de Resposta:**

```json
{
  "id": 0,
  "name": "string",
  "price": 0,
  "date": "dd/MM/yyyy",
  "variation": 0
}
```





**Rota:** <span style="color:orange">PUT</span> `/stock` 

**Corpo:** 

```json
{
  "id": 0,
  "name": "string",
  "price": 0,
  "date": "dd/MM/yyyy",
  "variation": 0
}
```

**Exemplo de Resposta:**

```json
{
  "id": 0,
  "name": "string",
  "price": 0,
  "date": "dd/MM/yyyy",
  "variation": 0
}
```



### Validação dos Dados

Os dados enviados para API devem seguir o  seguinte padrão:

- `name` : String **(obrigatório);**
- `price` : Double(6.2) **(obrigatório)**
- `date` : Date(dd/MM/yyyy) **(obrigatório)**
- `variation` : Double(3.2)  **(obrigatório)**
