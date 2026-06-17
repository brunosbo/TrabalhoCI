Nome: Bruno Simoes Borges de Oliveira
Trabalho de conclusao da disciplina de Integração continua.

Projeto: Clone do projeto de conclusão da disciplina de programação , em que possui testes unitários executados no Mocha.
Para que fossem gerados os relatórios, foi adicionado no projeto o Mochawesome. O Yarn também foi instalado para que possa executar os testes de mocha na integraçao contínua.

 - Para que a integração conínua funcione corretamente, foi adicionado no arquivo package.json:

"scripts": {
    "test": "mocha --reporter mochawesome --reporter-options reportDir=mochawesome-report"
}


 - Foi adicionado no projeto a pasta /.github/workflows o arquivo 01-Integrated-exec.yaml

 - no arquivo foi ajustado a execução manual, diretamente no github (workflow_dispatch), a execução automatica após commit (push branches) e o agendamento semanal (schedulo cron) .

 - no job da integraçao temos a execuçao no Ubuntu

 - os steps de execuçao, temos a instalaçao do node na ultima versao, a instalação do Yarn e as suas dependencias.

 - O comando Yarn test irá executar os tests do mocha. Na sequencia o relatório é gerado , com o comando Always garantindo que o mesmo será gravado, mesmo o teste quebrando. passando o diretório de gravaçao do relatório dentro do projeto.
