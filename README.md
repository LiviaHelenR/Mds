# 1. Introdução

Este documento descreve:

- A arquitetura geral do sistema IARA  
- O papel de cada componente  
- Os fluxos de dados entre os componentes  
- Como as informações são processadas do início ao fim  

---

# 2. Arquitetura Geral

Diagrama geral da arquitetura, mostrando todos os componentes e suas conexões.  
[Diagrama](https://drive.google.com/file/d/1Joo2wv4BY0snBw-iA11K9vUPkUAAzeQ5/view?usp=sharing)

---

# 3. Componentes da Arquitetura (Atores)

### **Usuário (Munícipe)**
Pessoa que utiliza o WhatsApp Pessoal para interagir com a IARA.



### **WhatsApp Pessoal**
- Canal onde o munícipe envia e recebe mensagens.  
- Não processa nada, apenas transmite as mensagens ao Botpress e exibe as respostas.



### **Botpress**
Responsável por:

- Interpretar mensagens do usuário (usa LLM)
- Entender a intenção do usuário  
- Realizar o diálogo  
- Decidir quando acionar o Middleware ou WhatsApp Flows  



### **WhatsApp Flows**
Usado quando o Botpress precisa:

- Coletar formulários  
- Obter dados estruturados (CPF, endereço, fotos etc.)

**Fluxo:**
- O Botpress solicita o Flow  
- O usuário preenche  
- O Flow devolve os dados ao Botpress


### **Middleware**
Camada intermediária responsável por:

- Receber pedidos do Botpress  
- Validar dados  
- Montar payloads  
- Chamar Sisgep-rest ou Sisgep-ngc  
- Converter respostas  
- Devolver ao Botpress o que deve ser respondido ao usuário  



### **Sisgep-rest**
- Endpoint REST  
- Recebe pedidos de inserção, consulta e atualização  
- Retorna status e dados processados  



### **Sisgep-ngc**
- Camada interna do SISGEP que aplica regras de negócio  
- Prepara dados para inserção no banco  
- Monta formulários que podem ser expostos pelo Sisgep-rest (quando aplicável)  



### **Banco de Dados (BD)**
Armazena dados como:

- Atendimentos  
- Reclamações  
- Solicitações  
- Usuários registrados  
- Outras informações de negócio  

---

## 4. Fluxos de Dados do Sistema

Abaixo estão descritos os principais fluxos de dados entre os componentes da IARA.



### **4.1 Fluxo de Conversação Inicial**

1. Usuário envia mensagem no WhatsApp.  
2. WhatsApp → envia para o Botpress via webhook.  
3. Botpress interpreta a mensagem e envia uma resposta padrão inicial.  



### **4.2 Fluxo de Formulário via WhatsApp Flows**

1. Botpress identifica que precisa de dados estruturados.  
2. Botpress → aciona WhatsApp Flows.  
3. Usuário preenche o formulário.  
4. WhatsApp Flows → envia os dados preenchidos ao Botpress.  
5. Botpress processa os dados e envia ao Middleware, se necessário.  



### **4.3 Fluxo de Cadastro de Reclamação (Fluxo Principal)**

> Este fluxo é o mesmo para qualquer tipo de reclamação.

1. Usuário escolhe o tipo de reclamação no WhatsApp.  
2. Botpress coleta dados (por mensagens ou Flow).  
3. Botpress envia os dados para o Middleware.  
4. Middleware valida e transforma o payload.  
5. Middleware → chama o Sisgep-rest.  
6. Sisgep-rest → aciona o Sisgep-ngc para aplicar regras de negócio.  
7. Sisgep-ngc → salva ou consulta dados no BD.  
8. Sisgep-rest → devolve resposta ao Middleware.  
9. Middleware → devolve resposta ao Botpress.  
10. Botpress → responde ao usuário no WhatsApp.  


### **4.4 Fluxo de Consulta (Acompanhar Protocolo)**

1. Usuário informa o número do protocolo.  
2. Botpress envia ao Middleware.  
3. Middleware chama o Sisgep-rest.  
4. Sisgep-rest consulta o BD via Sisgep-ngc.  
5. O status é retornado ao Middleware.  
6. Middleware devolve ao Botpress.  
7. Botpress responde ao usuário.  



 
