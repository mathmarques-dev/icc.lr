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

 ## 5. Requisitos não funcionais

| Código | Categoria | Requisito | Como medir |
|--------|-----------|-----------|------------|
| RNF01 | Usabilidade | O sistema deve possuir uma interface intuitiva, facilitando o acesso às funcionalidades de cadastro, consulta e solicitação de devolução. | Realizar testes de uso com usuários e verificar se conseguem executar as tarefas propostas. |
| RNF02 | Desempenho | O sistema deve ser otimizado para reduzir o tempo de carregamento das telas e das consultas. | Verificar se as principais telas e consultas respondem em até 2 segundos em condições normais de uso. |
| RNF03 | Segurança | O sistema deve possuir níveis de acesso, permitindo somente ao administrador atualizar o status dos itens e analisar as justificativas de devolução. | Testar as permissões dos perfis e confirmar que usuários comuns não conseguem executar ações administrativas. |
| RNF04 | Privacidade | O sistema deve restringir o acesso às informações pessoais dos usuários, evitando a exposição indevida de seus dados. | Verificar se informações pessoais não são exibidas publicamente sem necessidade. |
| RNF05 | Acessibilidade | A interface deve considerar as necessidades de pessoas com deficiência (PCDs), buscando facilitar o acesso e a utilização do sistema. | Testar a navegação por teclado, a legibilidade dos textos e a utilização de recursos de acessibilidade. |

## 6. Regras de negócio

- **RN01:** Somente o administrador pode atualizar o status dos itens cadastrados no sistema.
- **RN02:** A devolução de um item depende da análise das informações fornecidas pelo solicitante para comprovar a propriedade do objeto.
- **RN03:** Quando um item for devolvido, devem ser registrados o destinatário, a data e o horário da devolução.
- **RN04:** Os itens encontrados recebidos pelo setor de achados e perdidos devem ser cadastrados pelo administrador para que fiquem disponíveis no sistema.

- ## 7. Histórias de usuário

- Como **pessoa que perdeu um item**, quero **cadastrar uma descrição e uma foto do objeto perdido**, para **facilitar sua identificação e recuperação**.
- Como **pessoa que perdeu um item**, quero **consultar os itens encontrados no CEAGRI 2**, para **verificar se meu objeto foi localizado**.
- Como **pessoa que solicita a devolução de um item**, quero **enviar uma justificativa e fotos para comprovar que o objeto me pertence**, para **aumentar a possibilidade de recuperar meu pertence**.
- Como **administrador**, quero **cadastrar os itens encontrados que recebo**, para **disponibilizá-los para consulta no sistema**.
- Como **administrador**, quero **analisar as justificativas de devolução**, para **verificar se o solicitante é o verdadeiro proprietário do objeto**.
- Como **administrador**, quero **atualizar o status dos itens e registrar os dados das devoluções**, para **manter o controle dos objetos sob guarda e dos que já foram entregues**.

- ## 8. Dúvidas em aberto

- [ ] O sistema poderá ser acessado por qualquer pessoa ou somente por integrantes da comunidade acadêmica da UFRPE?
- [ ] Quais informações serão obrigatórias no cadastro de um item perdido?
- [ ] Como será confirmada a identidade da pessoa que solicita a devolução de um objeto?
- [ ] Por quanto tempo os itens encontrados permanecerão sob guarda?
- [ ] O que acontecerá com os objetos que não forem retirados após determinado período?
- [ ] Como serão protegidos os dados pessoais e as fotos enviados pelos usuários?
- [ ] Quais recursos específicos de acessibilidade serão implementados para pessoas com deficiência?

[UFRPE](https://www.ufrpe.br/)
