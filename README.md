# SA---Teste-de-Front-End
Testes de Denúncia e Login (Realizados com Cypress)
Linguagem — Função no Projeto
Linguagem	Função no Projeto
HTML	Estrutura visual das páginas
JavaScript	Lógica, validações, interatividade e testes Cypress
CSS	Estilização das páginas (cores, layout etc.)

Os testes foram desenvolvidos utilizando Cypress, garantindo que o formulário de denúncia, o menu, os textos, a navegação e toda a interface funcionem corretamente.

1️⃣ TESTES DA PÁGINA DE DENÚNCIA
✔️ Verificação dos Elementos da Interface

Esse teste confere se todos os elementos da página de denúncia aparecem corretamente, como:

Cabeçalho (logo + título FireLeaf)

Menu de navegação

Título principal: “Quer fazer uma denúncia?”

Formulário de denúncia

Campo Nome

Campo Local

Campo Relato

Upload de arquivo

Botão de enviar

Rodapé com mensagem final

Esse teste garante que a interface esteja completa e sem falhas visuais.

✔️ Teste dos Links de Navegação

Este teste verifica se os links do menu funcionam corretamente:

Início

Denunciar

Informações

Notícias

O Cypress clica nos links e confirma que a navegação ocorre sem erros.

✔️ Teste dos Campos Obrigatórios

Os campos:

Nome

Local

Relato

são validados para confirmar que possuem o atributo required, impedindo o envio de uma denúncia incompleta.

Isso garante que o usuário não consiga enviar o formulário vazio.

✔️ Teste do Botão Enviar

O teste apenas clica no botão Enviar Relato para garantir que ele está ativo e funcionando.

Mesmo sem validar envio, ele garante que o botão:

Está visível

Está clicável

Responde corretamente à ação

2️⃣ TESTES DA PÁGINA DE LOGIN
✔️ Verificação dos Elementos da Interface

Este teste garante que todos os elementos essenciais estão visíveis:

Logo da FireLeaf

Título "FireLeaf"

Campo de usuário (email)

Campo de senha

Botão Login

Link "Esqueceu a senha?"

Isso confirma que a interface carregou corretamente.

✔️ Impedir Login com Campos Vazios

Ao clicar em Login sem preencher nada, o sistema exibe:

"Por favor, preencha todos os campos."

A mensagem aparece em vermelho

Isso garante que não é possível realizar login sem digitar os dados.

✔️ Login com Credenciais Incorretas

O teste digita email e senha inválidos.

O sistema deve exibir:

"Usuário ou senha incorretos."

Isso confirma que a validação de login está funcionando.

✔️ Login Correto

Antes do teste, um usuário real é salvo no localStorage:

{
  "nome": "Carlos",
  "email": "carlos@gmail.com",
  "senha": "Senha@123"
}


O teste então:

Digita email correto

Digita senha correta

Clica no botão Login

E o sistema exibe:

"Login realizado com sucesso"

Isso confirma que o login funciona quando as credenciais estão corretas.

✔️ Clique no Link “Esqueceu a senha?”

O teste clica no link e verifica se o sistema mostra:

"Função de recuperação ainda não disponível."

Isso confirma que o link está funcionando corretamente.

✔️ RESUMO FINAL GERAL

Os testes automatizados com Cypress garantem que:

Página de Denúncia

✔ Interface funcionando
✔ Formulário completo
✔ Campos obrigatórios funcionando
✔ Menu funcional
✔ Botão de envio clicável

Página de Login

✔ Interface carregando corretamente
✔ Mensagem de erro para login vazio
✔ Mensagem de erro para credenciais erradas
✔ Login válido funcionando
✔ Link de recuperação funcional

