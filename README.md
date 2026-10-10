# Achados e Perdidos UFRPE: Documento de Requisitos

> Atividade prática de Levantamento de Requisitos (ICC / UFRPE).

## 1. Equipe

| Nome | Curso |
|------|-------|
| Matheus Marques | BCC |
| Davi Aguiar | BCC |
| João Guilherme | BCC |
| Alefe | BCC |
| Yan | BCC |
| Miguel | BCC |

## 2. Visão geral

**Problema:** Os objetos perdidos no bloco CEAGRI 2 da UFRPE podem não ser recuperados por seus donos devido à falta de um canal centralizado para registrar e consultar itens perdidos e encontrados.

**Solução proposta:** Desenvolver um sistema de Achados e Perdidos para o bloco CEAGRI 2, permitindo o cadastro e a consulta de itens perdidos e encontrados. O sistema permitirá que os usuários forneçam descrições e fotos para auxiliar na identificação dos objetos. Além disso, contará com um mecanismo de verificação de autenticidade para comprovar a propriedade dos itens e com o controle de status das devoluções.

**Escopo:** O sistema abrangerá o registro e a consulta de itens perdidos e encontrados no bloco CEAGRI 2, o envio de informações e fotos para comprovação de propriedade e o gerenciamento do status dos objetos pelo administrador. Não estão definidas, neste levantamento, funcionalidades de entrega dos itens fora do bloco ou de integração com outros setores da universidade.

## 3. Atores (usuários do sistema)

| Ator | Descrição | O que precisa fazer |
|------|-----------|---------------------|
| Pessoa que perdeu um item | Usuário que perdeu ou esqueceu um objeto no bloco CEAGRI 2 | Cadastrar itens perdidos, consultar itens encontrados e solicitar a devolução de um objeto, fornecendo informações que comprovem sua propriedade |
| Pessoa que encontrou um item | Usuário que encontrou um objeto no bloco CEAGRI 2 | Informar sobre o objeto encontrado para auxiliar na sua recuperação pelo dono |
| Administrador | Responsável pelo gerenciamento dos itens cadastrados no sistema | Cadastrar itens recebidos nos achados e perdidos, analisar as justificativas de devolução e atualizar o status dos itens |

## 4. Requisitos funcionais

### RF01: Cadastrar itens perdidos

- **Descrição:** O sistema deve permitir o cadastro de itens perdidos no bloco CEAGRI 2, possibilitando a inserção de uma descrição textual, uma foto do objeto e a identificação da pessoa que o perdeu.
- **Ator:** Pessoa que perdeu um item.
- **Prioridade:** Alta.
- **Critérios de aceitação:**
  - [ ] O usuário consegue informar uma descrição do item perdido.
  - [ ] O usuário consegue enviar uma foto do objeto.
  - [ ] O cadastro permite identificar a pessoa que perdeu o item.
  - [ ] As informações cadastradas ficam disponíveis no sistema.

### RF02: Cadastrar e listar itens encontrados

- **Descrição:** O sistema deve permitir que o administrador cadastre os itens encontrados e recebidos no setor de achados e perdidos do bloco CEAGRI 2. Após o cadastro, os itens devem ser armazenados no banco de dados e exibidos na seção de consulta de itens.
- **Ator:** Administrador.
- **Prioridade:** Alta.
- **Critérios de aceitação:**
  - [ ] O administrador consegue cadastrar um item encontrado.
  - [ ] Os dados do item são armazenados no banco de dados.
  - [ ] O item cadastrado aparece na listagem de itens encontrados.
  - [ ] Os usuários conseguem consultar os itens cadastrados.

### RF03: Verificar a autenticidade da solicitação de devolução

- **Descrição:** O sistema deve permitir que a pessoa que reivindica um item envie uma justificativa textual e fotos para comprovar que é a proprietária do objeto. O administrador poderá analisar as informações fornecidas para verificar a autenticidade da solicitação.
- **Ator:** Pessoa que perdeu um item e administrador.
- **Prioridade:** Alta.
- **Critérios de aceitação:**
  - [ ] O usuário consegue enviar uma justificativa textual sobre a propriedade do item.
  - [ ] O usuário consegue anexar fotos para auxiliar na comprovação.
  - [ ] O administrador consegue consultar as informações enviadas.
  - [ ] A solicitação fica disponível para análise do administrador.

### RF04: Consultar e atualizar o status dos itens

- **Descrição:** O sistema deve permitir o acompanhamento do estado de cada item, informando se ele ainda está sob guarda ou se já foi devolvido. Em caso de devolução, devem ser registrados o destinatário, a data e o horário da entrega. Somente o administrador poderá atualizar o status.
- **Ator:** Administrador.
- **Prioridade:** Alta.
- **Critérios de aceitação:**
  - [ ] O sistema identifica se o item ainda está sob guarda ou se foi devolvido.
  - [ ] O administrador consegue atualizar o status do item.
  - [ ] Quando um item for devolvido, o sistema registra para quem ele foi entregue.
  - [ ] A data e o horário da devolução ficam registrados.
  - [ ] Usuários sem perfil de administrador não conseguem atualizar o status do item.
