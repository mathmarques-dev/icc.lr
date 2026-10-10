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
