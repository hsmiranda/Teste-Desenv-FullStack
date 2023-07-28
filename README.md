# Teste Técnico - Desenvolvedor(a) Full Stack

Quando finalizar o teste, publique tudo no seu [Github](https://github.com) de modo público e envie por email com o título `[Teste Full Stack] Finalizado` para o organizador.

## Backend

Desenvolver uma **API JSON RESTful** em **Java**, utilizando os frameworks *Quarkus ou Spring boot*, com os métodos (`GET`, `POST`, `PUT`, `DELETE`).
Salvar dados em um banco de dados MySQL, utilizando **JPA**.

### Especificação

Monte uma base de veículo com a seguinte estrutura:

```
veiculo:   string
marca:     string
ano:       integer
descricao: String
vendido:   boolean
created:   datetime
updated:   datetime
cassi:     String
preco:     ??? (Escolha livre)
```

Utilize **PostgreSQL** ou **H2** ou **SQLite** através do **JPA** para armazenar os dados que a **API** irá consumir.

### API Endpoint

`GET /veiculos`

Retorna todos os veículos

---

`GET /veiculos`

Retorna os veículos de acordo com filtros passados através de query string

---

`GET /veiculos/{id}`

Retorna os detalhes do veículo

---

`POST /veiculos`

Adiciona um novo veículo

---

`PUT /veiculos/{id}`

Atualiza os dados de um veículo

---

`DELETE /veiculos/{id}`

Apaga o veículo


## Frontend

Desenvolver **UI (User Interface)** baseado no escopo que está na pasta [layout](https://github.com/hsmiranda/Teste-Desenv-FullStack/tree/master/layout), utilizando HTML, CSS e Javascript (Pode usar jQuery, Vue.js, Angular ou React ou qualquer outro framework Web).

### Especificação

- Consumir **API** criada acima
- Criar uma tela que tenha:
    - Listagem de veículos
    - Detalhe do veículo
    - Busca
    - Formulário de novo/edição de veículos

### Dica

Você poderá utilizar bootstrap para auxiliar no desenvolvimento da interface, encontrado através do link:

- http://getbootstrap.com/css/

## Dúvida

Se tiver qualquer dúvida sobre esse teste, envie um email ou abra um issue.

## Regras de negócios

As regras de negocio podem ser implementadas no backend, frontend ou em ambos ficando a criterio do tipo de prova.

- RN001 - Não pode haver veiculos com o mesmo numero de chassi.
- RN002 - O sistema não deve permite preços negativos.
- RN003 - O sistema não deve permitir que veiculos tenham no cadastro ou atualização, ano supeior ao corrente, por exemplo: o ano atual é 2023 e um veiculo estão tentando cadastrar com o ano 2024.
- RN004 - A bvusca deverá exibir até no máximo 5 resultados por vez, ou seja deve paginar de 5 em 5 os resultados.
- RN005 - O sistema deve ser seguro, não permitindo que códigos maliciosos sejam inseridos no meio dos textos.