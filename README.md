Pipeline de Teste com GitHub Actions
Descrição

Esta pipeline executa testes simulados, gera um relatório HTML e disponibiliza o resultado como artefato no GitHub Actions.

Ambiente
runs-on: windows-latest

A execução ocorre em um ambiente Windows fornecido pelo GitHub.

Gatilhos
Push nas branches main e master
Execução manual (workflow_dispatch)
Execução automática a cada 20 minutos
schedule:
  - cron: '*/20 * * * *'
Etapas
Checkout do código.
Execução dos testes simulados.
Geração do relatório HTML.
Upload do relatório como artefato.
Relatório

O arquivo index.html é gerado na pasta:

relatorio-pasta/

e publicado como artefato com o nome:

meu-relatorio-de-testes

O relatório fica disponível para download por 7 dias na aba Actions do GitHub.
