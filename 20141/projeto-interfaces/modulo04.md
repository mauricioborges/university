# Atividade: Elementos iniciais do projeto de Interfaces

Realize com o seu grupo a definição inicial do projeto de interfaces a ser desenvolvido como tarefa prática. Esta definição deve ser entregue até o final desta semana de atividades. Verifique o enunciado do trabalho prático (consulte o README.md) e *preencha os itens indicados na introdução* (item 1 do enunciado) . A versão final do projeto deve ser entregue na sexta semana de aula e valerá 5,5 pontos do GA.

A entrega da definição inicial do projeto nesta tarefa não valerá nota!

## Resolução

### Apresentação inicial do trabalho, descrevendo sucintamente o sistema

Para uma empresa de desenvolvimento de software, em função dos processos assíncronos de desenvolvimento, testes de aceitação e posterior entrega em produção, há um sistema para controle dos deploys efetuados em diversos servidores na cloud privada que a empresa possui. Para gerenciamento destes deploys eram utilizadas planilhas excel e arquivos de texto. Em função do excesso de sobreposição de versões em diversos ambientes, optou-se por criar um pequeno sistema web que:
* exiba o status de todos os servidores: aplicações em execução, solicitantes, data de deploy, etc
* forneça acesso ao andamento de um deploy, que deve ser consultado em um REST service de uma ferramenta externa (jenkins-ci e rundeck)
* envie notificações por e-mail/skype chat de quando um deploy request colidiu com outro

### Descrição de um cenário geral de uso do sistema

```
Como responsável pelos testes de aceitação
Quando qualquer pessoa solicitar um deploy em ambiente de UAT (user acceptance test)
Então o sistema deve notificar do inicio de atualização
E avisar também o solicitante do deploy
E avisar também a pessoa que realizou o último deploy em execução
```  
    

### Descrição do tipo de público alvo
O público alvo do sistema é tipicamente uma equipe envolvida no desenvolvimento de software tradicional:
* gerentes de projeto
* desenvolvedores
* analistas de testes e qualidade
* coordenadores e gestores de pessoas

### Apresentação sucinta das alternativas tecnológicas a serem consideradas
Em função da relativa simplicidade tecnológica do sistema, que basicamente será composto de atualizações em real-time e consulta a REST services, a alternativa tecnológica mais adequada, em princípio, seria o uso de um framework Python ou Ruby para desenvolvimento leve, em conjunto com Framework JS para desenvolvimento de interfaces como o Twitter Bootstrap.

Um exemplo seria o deploynator, da Etsy (http://codeascraft.com/2010/05/20/quantum-of-deployment/)

