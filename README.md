# library-backend

Projeto desenvolvido em JAVA Spring Boot.

Dependências utilizadas:<br />
 *DevTools.<br />
 *Web (Pelo fato de ser uma APIRest).<br />
 *JPA.<br />
 *Postgres (Bando de dados relacional).<br />
<br />
No arquivo application.properties possui todas as informações de conexão ao BD: url, username and password<br />
(diretório: \library-backend\backEnd\apilibrary\src\main\resources): <br />

<h3>Instalação e execução</h3><br />
1. Baixe ou faça o clone desse projeto<br />
2. Abra o Eclipe-> File -> import -> Existing Maven Projects -> Informar o caminho do projeto -> ao carregar você irá selecionar o projeto -> Finish.<br />
3. Aguardar o Eclipse baixar todas as dependencias do projeto.<br />
4. Dentro do package <i>"com.indt.books.apilibrary"</i> tem a Classe para executar o projeto: Clicar em cima da Classe <i>"ApilibraryApplication.java"</i> com o botão direito do mouse -> Run As -> Java Aplication.
5. Esperar o SpringBook iniciar o proejto.

<h3>Rotas da aplicação</h3><br />
<ul>
  <li>
    <strong>GET /books:</strong> Essa rota retorna um objeto, em formato JSON, com todas os livros cadastrados no banco.
  </li>
  <li>
    <strong>GET /book/id:</strong> Essa rota um retorna objeto, em formato JSON, com todas as informações de um único livro. Lembrando que nos parâmetros da rota é preciso passar o id do livro.
  </li>
  <li>
    <strong>POST /book:</strong> A rota deve receber nome, autor e isbn dentro do corpo da requisição. Ao cadastrar um novo livro, ele deve ser armazenado dentro de um objeto no formato JSON:  { "id": 1, "nome": "Livro 1", "autor": "Autor 1","isbn": 14, "valid": true }. Obs: Como default, o valid sempre será true ao ser criado um novo livro.
  </li>
  <li>
    <strong>DELETE /books/id:</strong>Essa rota deleta um livro com o id presente nos parâmetros da rota
  </li>
  <li>
    <strong>PUT /book:</strong> A rota alterar nome, autor, isbn do livro;
  </li>
  <li>
    <strong>GET /book/search:</strong> A rota retorna dados de livros que contenham o nome parecido com o parâmetro repassado na rota e isValid tem que ser true.
  </li>
    <li>
    <strong>PATCH /book/valid/id:</strong> A rota somente alterar o valid(disponível ou indisponível) do livro para true or false.
  </li>
 </ul>
