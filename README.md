# Análise componente Breadcrumb

### Listar as rotas de um fluxo e cada uma separada por ">":

- Adicionar o caractere ">" entre cada rota na exibição.
  
## Etapa atual do fluxo fica em negrito:

- Já está sendo aplicado uma classe de estilo `font-bold` à **etapa atual**. `selectedStyle`.
  
## Quando o usuário navegar para uma etapa, o texto fica com um underline:

- Para adicionar um sublinhado ao texto quando o usuário navegar para uma **etapa**, será necessário adicionar uma verificação semelhante à aplicada para o estilo negrito, mas com uma classe de sublinhado.


# Documentação do Endpoint

Este endpoint é um exemplo

## Método

`POST /api/createuser`

## Body

- `name` - string (obrigatório)
- `typePerson` - string (obrigatório)
- `cpf` - string (obrigatório)
- `cnpj` - string (não obrigatório)
- `cellPhone` number (obrigatório)
- `telephone` number (obrigatório)
- `email` string (obrigatório)
- `cep` string (obrigatório)
- `publicPlace` string (obrigatório)
- `addressNumber` number (obrigatório)
- `complement` string (obrigatório)
- `city` string (obrigatório)
- `district` string (obrigatório)
- `state` string (obrigatório)

## Respostas

### Sucesso (200 OK)

Retorna um objeto JSON com os detalhes do usuário.

Exemplo de resposta:

```json
{
  "id": 123,
  "nome": "João da Silva",
  "personType": "PF",
  "cpf": "636.726.909-61",
  "cnpj": null,
  "email": "joao@example.com",
  "cep": "78142186",
  "publicPlace": "Rua",
  "addressNumber": 234,
  "complement": "Casa 2",
  "city": "São Paulo",
  "district": "Pinheiros",
  "state": "São Paulo",
}
```

## Sucesso (Created)

- **201 Created**: Cadastrado com sucesso! Número protocolo, *número-protocolo*.

## Erros Possíveis

- **404 Not Found**: Se o usuário com o ID especificado não for encontrado.
- **400 Bad Request**: Se o ID fornecido não for um número inteiro válido.
- **409 Bad Request**: Usuário já cadastrado.
- **500 Bad Request**:  *Nome do usuário*. Tente novamente mais tarde.
