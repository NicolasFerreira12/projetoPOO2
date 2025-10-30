# Nicolas Ferreira Bicudo Duarte - 00000851339
# 
# Projeto 2 - Programação Orientada a Objetos

**● Descrição:**
Este projeto foi desenvolvido para a disciplina **Programação Orientada a Objetos**, na universidade **Universidade Católica de Pernambuco - UNICAP**.

===================================================

O sistema simula o gerenciamento de uma **Clínica**, permitindo:

**● Funcionalidades:**

- Cadastro de pacientes, médicos e locais
- Agendamento de consultas
- Listagem de todas as consultas
- Relatórios estratégicos para tomada de decisão
  
**● Relatórios Disponíveis:**

- Total de médicos cadastrados
- Consultas por médico
- Consultas por paciente
- Médico com mais consultas
- Consultas realizadas
- Total de pacientes cadastrados

A arquitetura segue o padrão em camadas:
- **model** → entidades principais (Paciente, Medico, Consulta)
- **repository** → armazenamento dos dados em memória
- **service** → regras de negócio e relatórios
- **menu** → interação com o usuário via console

===================================================

**● Exemplos de Uso:**

1. Cadastre pelo menos 1 médico, 1 paciente e 1 local;

2. Agende consultas através do menu;

3. Acesse os relatórios para visualizar estatísticas;


===================================================

**● Para executar:**
  
- git clone https://github.com/NicolasFerreira12/projetoPOO2

//////////////////

**src/clinica/model:**

1. Pessoa.java: 

Funcionamento: Classe base para representar qualquer pessoa no sistema, com dados básicos de identificação e contato. Serve como superclasse para Paciente e Medico.


2. Paciente.java: 

Funcionamento:Representa um paciente da clínica, herdando de Pessoa e adicionando histórico médico, listas de consultas/check-ups e status de desconto para integração com outros sistemas.


3. Medico.java: 

Funcionamento: Representa um médico da clínica, com especialidade, CRM e lista de consultas agendadas. Herda de Pessoa.


4. Consulta.java: 

Funcionamento: Representa uma consulta médica com dados do paciente, médico, data/hora, tipo e resultado. Usa IDs para referenciar outras entidades.


5. CheckUp.java: 

Funcionamento: Representa um check-up rápido com métricas de saúde básicas. Tem método para calcular IMC e marcar como completo.


6. Local.java (Clinica): 

Funcionamento: Representa um local físico onde as consultas/check-ups acontecem. Usado por todos os sistemas.


7. Pagamento.java (Clinica): 

Funcionamento: Representa um pagamento realizado no sistema da clínica. Pode ser reutilizado pelos outros sistemas.


**src/eventos/model:**

1. ClinicaService.java: 

Funcionamento: Serviço que gerencia todas as operações da clínica: cadastro de pacientes/médicos, agendamentos, check-ups e pagamentos. Fornece métodos para análise de dados.

**src/eventos/model:**

1. Evento.java: 

Funcionamento: Classe base para representar eventos (palestras, oficinas, shows). Gerencia participantes e capacidade do local.


2. Palestra.java: 

Funcionamento: Especialização de Evento para palestras de saúde, com palestrante, tema e duração específicos.


3. Oficina.java: 

Funcionamento: Representa oficinas práticas com instrutor, material necessário e controle de vagas disponíveis.


4. Show.java: 

Funcionamento: Representa shows culturais com artista, gênero musical e informação sobre open bar.


5. Local.java (Eventos): 

Funcionamento: Local específico para eventos, com capacidade e tipo adequados para palestras, oficinas ou shows.


6. Pagamento.java (Eventos): 

Funcionamento: Pagamentos específicos para eventos (ingressos, inscrições em oficinas, etc.).


**src/eventos/service:**

1. EventoService.java: 

Funcionamento: Serviço que gerencia todos os aspectos dos eventos: cadastro, inscrições, controle de capacidade, geração de vouchers e estatísticas de participação.


**src/restaurante/model:**

1. Cardapio.java: 

Funcionamento: Representa o cardápio do restaurante, contendo itens individuais e combos especiais. Oferece método para filtrar itens funcionais.


2. ItemCardapio.java: 

Funcionamento: Representa um item individual do cardápio com informações nutricionais, restrições alimentares e método para aplicar descontos.


3. Combo.java: 

Funcionamento: Representa combos de refeições com cálculo automático de descontos e economia. Combos especiais têm desconto maior.


4. Voucher.java: 

Funcionamento: Representa vouchers de desconto com validação de uso, cálculo de desconto e controle de data de utilização.


5. Local.java (Restaurante): 

Funcionamento: Local específico para restaurante, com informações sobre mesas e serviço de delivery.


6. Pagamento.java (Restaurante): 

Funcionamento: Pagamento específico para restaurante, com suporte a descontos de voucher e cálculo de valor final.


**src/restaurante/service:**

1. RestauranteService.java: 

Funcionamento: Serviço completo do restaurante gerencia cardápios, combos, vouchers, pagamentos e histórico de clientes. Oferece métodos para análise de ticket médio, utilização de vouchers e estatísticas de vendas.
