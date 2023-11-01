Step 1

- Criar um objeto mock para oq seria um TODO e outro para Reminder
- Criar controller que guarda uma Array<Object>, sendo esses objetos TODO e Reminder criados anteriormente
- Criar uma no HTML um form com um button de submit and um ul para preencher com a list the TODO e Reminder
- Add um evento ao submit do form
- Criar uma view que sera passada ao controller, essa view sera um objeto com um metodo render
- Usar typeof na view para o controller, somente para exemplo
- Chamar o metodo render da view passando as tasks dentro handler do submit do form
- Mencionar que a list do controller nesse momento aceita qualquer objeto seja la qual ele ou quais propriedades ele tem
- Mencionar que o o TS ja contem os types dos elements do DOM como por exemplo HTMLElement e Event

Step 2

Criar classes e interfaces para TODO e Reminder, mostrar como a interface garante o contrato que deve ser seguido para que toda task tenha um metodo render que sera usado na VIEW.

- Criar uma classe TODO e suas propriedades, nao add o render ainda
- Criar uma classe Reminder e suas propriedades, nao add o render ainda
- Mostrar como pederiamos criar um Array<TODO|Reminder>
- Criar uma interface chamada Task que ira manter o contrato para todas as Tasks, sejam TODO ou Reminder, nesse momento add o metodo render
- Metodo render somente faz JSON.stringify(this)
- Alterar o controller para que ele guarde um Array<Task> assim mostrando como a interface gera um contrato que deve ser seguido por todos os elementos desta lista

Step 3

Add um pouco mais de estrutura somente para brincar com TS, criando um enum de NotificationPlatform e alguns Utils para reforcar como e feito a tipagem de metodos. Mostrar como o enum reforca a estrutura nao deixando valores errados serem added a lista de notifications

- Criar o enum de NotificationPlatform
- Alterar o Reminder para usar Array<NotificationPlatform> assim enfatizando o erro criado no contrutor onde 'EMAIL' nao e mais valido
- Criar o UUID e o DateUtils somente para reenfatizar como se add type nas props de um metodo e se define o type do retorno
- Chamar UUID e DateUtils dentro das classes TODO e Reminder
- Melhorar o render para nao ser somente JSON.stringify(this)

Final (Master)

Introduzir mais um enum, de Modes onde vamos usar ele para gerenciar com o que estamos lidando um TODO ou um Reminder.

- Criar o enum de Modes
- Add no HTML o form com fieldset e o button que faz o toggle entre os modos
- No codigo criar um handler para o toggle e impl a troca de modo dentro do context do controller
- Criar no metodo render a troca de Mode e depois chamar o render no controller depois de trocar o modo do context
- Add 2 metodos no view para poder recuperar as infos do form e criar ou TODO ou Reminder com essas infos
- O controller deve utilizar dos metodos da View para conseguir pegar um Todo ou Reminder direto da view
- Add o TODO ou Reminder a lista de Tasks e depois chamar o render novamente.