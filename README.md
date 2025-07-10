## 🧪 Testes Automatizados com Cypress

Você gpsta de praticidade no seu dia a dia, com um robô fazendo as coisas pra você? Pois eu simplesmente A-D-O-R-O!
Então, se você é do meu time, vem dar uma olhada no que conseguimos realizar com o **Cypress**, uma das ferramentas mais populares para testes end-to-end em aplicações web modernas.

Os arquivos abaixo fazem parte dos testes realizados na aplicação fictícia **Alura Pic**, fornecida para fins educacionais.

---

### 🌐 alura-pic.cy.js

Este arquivo contém uma suíte de testes para o **formulário de registro** da aplicação [Alura Pic](https://alura-fotos.herokuapp.com). Os testes validam os seguintes cenários:

#### 🔎 Casos de teste implementados:

* **Validação de campos obrigatórios** (mensagens como “Email is required!”, “Password is required!” etc.)
* **Email inválido**
* **Nome completo com menos de 2 caracteres**
* **Nome de usuário com letra maiúscula**
* **Nome de usuário com menos de 2 caracteres**
* **Validação combinada de nome de usuário (minúsculo + mínimo 2 caracteres)**
* **Senha com menos de 8 caracteres**
* **Cadastro de múltiplos usuários a partir de um JSON** (utilizando `cy.fixture()`)

📂 *Recurso adicional:* Os dados de usuários utilizados para o cadastro estão em `fixtures/usuarios.json`.

🔗 Arquivo: `alura-pic.cy.js`

📽️ Demonstração visual: 

https://user-images.githubusercontent.com/67244332/216509721-7822e1a4-f8eb-4f8c-96f3-ca6e9f7c3276.mp4

---

### 🔌 api-alurapic.cy.js

Este arquivo testa diretamente a **API REST** da aplicação.

#### 🧾 Casos de teste:

* **Requisição GET para buscar fotos do usuário "flavio"**

  * Verifica status 200
  * Confirma que o corpo da resposta não está vazio
  * Verifica se a primeira foto possui uma descrição específica

* **Requisição POST para login via API**

  * Verifica status 200
  * Valida propriedades do corpo da resposta (`id`, `email`)
  * Usa variáveis de ambiente com `Cypress.env()` para enviar os dados

🔗 Arquivo: `api-alurapic.cy.js`

📽️ Demonstração visual: 

https://user-images.githubusercontent.com/67244332/216510450-f1a6e1d5-5ba3-41a5-b927-f620990eadd2.mp4

---

### 📌 Observações

* Os testes foram organizados com `describe()` e `it()` seguindo as boas práticas do Cypress/Mocha.
* Todos os testes estão prontos para serem executados no Cypress Dashboard.
* O uso de `fixtures` torna os testes mais escaláveis e reutilizáveis.

---

🚀 *Esses testes são parte do meu aprendizado em automação e serão expandidos conforme avanço com novas funcionalidades e integrações.*
