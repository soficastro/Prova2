# Folha de pagamento
# *Funcionalidades*
"O sistema consiste de um banco de dados de empregados de uma empresa além dos seus dados associados tais como cartões
de ponto. O sistema deve pagar cada empregado. Empregados devem receber o salário correto, no momento correto, usando o método que eles preferem. Além do mais, várias taxas e impostos são deduzidos do seu salário."
- Adicionar, editar e remover funcionários dos tipos assalariado, horista e assalariado comissionado.
- Lançar cartão de ponto, resultado de venda e taxa de serviço aos funcionários.
- Lançar folha de pagamento do dia, evetuando os devidos pagamentos.
- Desfazer as ações descritas anteriormente (Undo/Redo) .

# Padrões de projeto utilizados
- Memento: Para que fosse executada a funcionalidade Undo/Redo, foi implementado o padrão de projeto Memento sobre a classe Systema, que atua como "originator", assim, são salvos estados desta classe sempre que necessário. A classe Memento foi implementada para que sirva como uma cópia do estado do objeto da classe Systema, enquanto a classe Caretaker é responsável pelo gerenciamento desses mementos. 
- Builder: Com o objetivo de melhorar a construção de objetos da classe Employee, que possui muitos atributos e 3 subclasses, foi utilizado o padrão de projeto Builder. Para isso, foram criadas as classes EmployeeBuilder, HourlyBuilder, ComissionedBuilder e SalariedBuilder, aninhadas às classes Employee, Hourly, Comissioned, e Salaried, respectivamente. 
