
# 3. DOCUMENTO DE ESPECIFICAÇÃO DE REQUISITOS DE SOFTWARE
[Entrega2_Grupo1_Projeto_Eixo3_CuidaMente.docx](https://github.com/user-attachments/files/22585984/Entrega2_Grupo1_Projeto_Eixo3_CuidaMente.docx)


## 3.1 Objetivos deste documento
Descrever e especificar as necessidades do Grupo 1 do Eixo 3 do Curso de Sistemas de Informação da PUC Minas que devem ser atendidas pelo projeto CuidaMente – Tecnologia inclusiva para a saúde mental. 

## 3.2 Escopo do produto


### 3.2.1 Nome do produto e seus componentes principais
O produto será denominado CuidaMente – Tecnologia inclusiva para a saúde mental.

### 3.2.2 Missão do produto
Facilitar a conexão entre profissional da saúde mental e pessoas interessadas nesse serviço.  

### 3.2.3 Limites do produto
O CuidaMente não oferece plataforma para vídeo chamadas, chamadas de áudio ou ligação telefônica, assim como não oferece infraestrutura. O CuidaMente não faz intermediação financeira. 

### 3.2.4 Benefícios do produto


| # | Benefício | Valor para o Cliente |
|--------------------|------------------------------------|----------------------------------------|
|1	| Facilidade no cadastro de dados |	Essencial |
|2 | Facilidade na recuperação de informações | Essencial | 
|3 | Segurança no cadastro de cadastros | Essencial | 
|4	| Interface simples e intuitiva	| Essencial | 

## 3.3 Descrição geral do produto

### 3.3.1 Requisitos Funcionais

| Código | Requisito Funcional (Funcionalidade) | Descrição |
|--------------------|------------------------------------|----------------------------------------|
| RF1 | Cadastro de Profissional |	O sistema deve permitir que profissionais se cadastrem e criem um perfil |
| RF2 |	Edição de Perfil 	| O sistema deve permitir editar dados |
| RF3	| Estatísticas de Perfil  |	O sistema deve exibir estatísticas de visualização do perfil, sem identificar individualmente os visitantes |
| RF4 |	Restrições 	| O sistema não deve permitir o cadastro de visitantes (potenciais pacientes) |
| RF5 |	Contato com profissional 	| O visitante deve ter acesso a informações para iniciar comunicação externa com o profissional |
| RF6 |	Administrativa 	| O administrador deve poder gerenciar cadastros (editar, inativar, excluir) |
| RF7 |	Administrativa 	| O administrador deve poder aceitar ou rejeitar publicação de perfil |
| RF8 |	Administrativa 	| O administrador deve poder emitir relatórios sobre os cadastros e estatísticas gerais |

### 3.3.2 Requisitos Não Funcionais

| Código | Requisito Não Funcional (Restrição) |
|--------------------|------------------------------------|
| RNF1 | Ambiente | Multiplataforma |
| RNF2 | Segurança | O produto deve restringir o acesso por meio de senhas individuais para o usuário |
| RNF3 |	Acessibilidade | O produto deve atender ao nível A de conformidade com as diretrizes de acessibilidade |
| RNF4 |	Responsividade  |	O produto deve ser capaz de se adaptar e apresentar o conteúdo de forma otimizada em diferentes tamanhos de telas e dispositivos |
| RNF5 |	Escalabilidade  |	O produto deve suportar o acesso até 1000 acessos simultâneos sem comprometer significativamente a performance  |
| RNF6 |	Usabilidade |	O produto deve apresentar layout simples e intuitivo, garantindo que o visitante consiga navegar com no máximo 3 cliques para encontrar um profissional  |
| RNF7 |	Multiplataforma  |	O sistema deve funcionar em navegadores desktop e dispositivos móveis |

### 3.3.3 Usuários 

| Ator | Descrição |
|--------------------|------------------------------------|
| Administrador |Usuário gerente do sistema, possui acesso geral ao sistema |
| Profissional  |	Usuário que será cadastrado no sistema para oferecer seus serviços. Terá acesso à criação e edição de perfil e dados básicos, relatórios sobre estatísticas de visitas em seu perfil |
| Visitante/Potencial Paciente |	Usuário que acessa o sistema para buscar profissionais |

## 3.4 Modelagem do Sistema

### 3.4.1 Diagrama de Casos de Uso
Como observado no diagrama de casos de uso da Figura 1, o Profissional poderá cadastrar e editar perfil no sistema, enquanto o Administrador poderá gerenciar cadastros, emitir relatórios, contactar profissional e editar perfis, já o Visitante/Potencial Paciente poderá contactar o Profissional. 

#### Figura 1: Diagrama de Casos de Uso do Sistema.

![dcu]<img width="1710" height="796" alt="Screenshot 2025-09-28 022559" src="https://github.com/user-attachments/assets/fc81e943-4f48-4e49-a552-fe05fe97a817" />

 
### 3.4.2 Descrições de Casos de Uso

### Cadastrar Perfil (CSU01) 

Sumário: O Profissional preenche o formulário para cadastro de perfil (inclusão) 
Ator Primário: Profissional 
Ator Secundário: Administrador 
Pré-condições: Profissional deve ter acesso à internet e fornecer dados básicos. 
Fluxo Principal: 

O Profissional preenche o formulário inicial (Nome Completo, nº do CRP, E-mail para contacto, Telefone, Senha, Confirmação de senha) para cadastrar um perfil no Sistema. 
O Sistema apresenta a operação que pode ser realizada: registrar cadastro.  
O Profissional seleciona a operação desejada: Registrar Cadastro ou opta por finalizar o caso de uso. 
Se a operação desejada for Registrar Cadastro, o Sistema inclui o Profissional no registro de cadastro e apresenta as operações que podem ser realizadas: editar perfil. 
O Profissional seleciona a operação desejada: Editar Perfil, ou opta por finalizar o caso de uso. 

Fluxo Alternativo (1): Registrar Cadastro 
O Profissional requisita o registro de cadastro de perfil. 
O Sistema verifica a validade dos dados.  
Se os dados forem válidos, o Sistema verifica se o Profissional já está cadastrado. Se sim, o Sistema reporta o fato e apresenta as operações que podem ser realizadas: Fazer Login ou Solicitar Troca de Senha, ou opta por finalizar o caso de uso; caso contrário, o Profissional é registrado no Sistema. 
Se os dados não forem válidos, o Sistema reporta o fato e solicita novos dados e repete a verificação. 

Fluxo Alternativo (2): Editar Perfil 
O Profissional edita um ou mais detalhes a serem exibidos no perfil (foto, modalidade de atendimento, localização, valor da sessão/ tempo de duração, abordagem principal, descrição), solicita a atualização e publicação. 
O Administrador aceita ou rejeita a solicitação de publicação. 

Pós-condições: Um profissional foi inserido. A publicação do perfil fica sujeita a análise do Administrador. 

 

### Fazer Login (CSU02) 

Sumário: O Profissional fornece dados de usuário e senha (acesso)
Ator Primário: Profissional 
Ator Secundário: Administrador 
Pré-condições: Profissional deve ter acesso à internet e já estar cadastrado
Fluxo Principal: 

O Profissional preenche os campos de Usuário e Senha e solicita acesso  
O Sistema verifica a validade dos dados. Se os dados forem válidos, o Profissional acessa seu perfil. Se os dados não forem válidos, o Sistema reporta o fato e apresenta as operações que podem ser realizadas: tentar novamente ou solicitar troca de senha. 
O Profissional seleciona a operação desejada: Tentar Novamente, Solicitar Troca de Senha ou opta por finalizar o caso de uso. 

Fluxo Alternativo (1): Tentar Novamente 
Repete o fluxo principal 

Fluxo Alternativo (2): Solicitar Troca de Senha 
O Profissional fornece o e-mail de usuário e solicita a troca de senha. 
O Sistema envia um link para o e-mail informado. 
O Profissional solicita a alteração da senha. O Sistema verifica a validade dos dados e, se eles forem válidos, altera a senha no cadastro do Profissional, caso contrário, reporta o fato. 

Pós-condições:  
 

### Buscar Profissional (CSU03) 

Sumário: O Visitante busca profissionais utilizando filtros (consulta) 
Ator Primário: Visitante 
Pré-condições: O sistema deve estar disponível online. 
Fluxo Principal: 

O Visitante acessa a página inicial. 
O Visitante digita um nome ou seleciona filtros (especialidade, localização, modalidade de atendimento). 
O Sistema processa a busca. 
O Sistema exibe a lista de profissionais compatíveis. 

Fluxo Alternativo (1): Nenhum resultado encontrado 
O Sistema exibe mensagem de que não há resultados para os filtros escolhidos e sugere ajustes de pesquisa. 

Pós-condições: O visitante obtém uma lista de profissionais disponíveis conforme os critérios aplicados. 


### Gerenciar Cadastros (CSU04) 

Sumário: O Administrador fornece dados de usuário e senha (acesso). 
Ator Primário: Administrador 
Ator Secundário:  
Pré-condições: O Administrador precisa já estar cadastrado 
Fluxo Principal: 

O Administrador preenche os campos de Usuário e Senha  
O Sistema verifica a validade dos dados. Se os dados forem válidos, o Administrador acessa o Sistema. Se os dados não forem válidos, o Sistema reporta o fato e apresenta as operações que podem ser realizadas: tentar novamente ou solicitar troca de senha. 
O Administrador seleciona a operação desejada: Tentar Novamente, Solicitar Troca de Senha ou opta por finalizar o caso de uso. 

Fluxo Alternativo (1): Solicitar Troca de Senha 

O Profissional seleciona a opção solicitar troca de senha. 
O Sistema solicita o e-mail cadastrado 
O Sistema envia instruções de redefinição de senha. 

Pós-condições: O Profissional consegue acessar o sistema. Dependendo da ação realizada, ele pode ter: 
Tentado login com sucesso e acessado o sistema; 
Solicitada redefinição de senha; 
Encontrados dados inválidos, permanecendo na tela de login até correção. 

 
### Contactar Profissional (CSU05) 

Sumário: O Visitante inicia contato direto com um profissional. 
Ator Primário: Visitante 
Ator Secundário: Administrador 
Pré-condições: O profissional deve ter cadastro válido e perfil publicado. 
Fluxo Principal: 

O Visitante acessa o perfil de um profissional. 
O Sistema exibe os meios de contato disponíveis 
O Visitante escolhe o meio de contato. 
O Sistema redireciona o Visitante para o aplicativo externo correspondente (WhatsApp ou e-mail). 


Fluxo Alternativo (1): Contato indisponível 
Caso um dos meios de contato esteja temporariamente indisponível, o Sistema notifica o visitante e sugere outra opção disponível. 

Pós-condições: A comunicação entre visitante e profissional é iniciada fora da plataforma. 

 

### Editar Perfil (CSU06) 

Sumário: O profissional deve já ter um cadastro válido no sistema. 
Ator Primário: Profissional
Ator Secundário: Administrador 
Pré-condições: O profissional deve já ter um cadastro válido no sistema. O profissional deve estar autenticado (login realizado). 
Fluxo Principal: 

O Profissional acessa seu perfil. 
O Sistema apresenta os dados já cadastrados. 
O Profissional seleciona a opção Editar Perfil. 
O Profissional altera os campos desejados (foto, localização, modalidade de atendimento, abordagem principal, valor da sessão, descrição). 
O Profissional confirma a atualização. 
O Sistema registra a solicitação de alteração e a envia para análise do Administrador. 
O Administrador valida e publica a atualização. 


Fluxo Alternativo (1): Dados inválidos 
O Sistema identifica inconsistências (ex.: e-mail inválido, número de CRP duplicado). 
O Sistema reporta o erro e solicita correção dos dados 
 

Pós-condições: O perfil é atualizado e fica sujeito à validação/publicação pelo Administrador. 

 
### Emitir Relatórios (CSU08) 

Sumário: O profissional deve já ter um cadastro válido no sistema. 
Ator Primário: Administrador 
Pré-condições: O administrador deve estar autenticado. 
Fluxo Principal: 

O Administrador acessa o painel administrativo. 
O Sistema apresenta opções de relatórios (número de profissionais cadastrados, estatísticas de visitas a perfis, relatórios por especialidade etc.). 
O Administrador seleciona o tipo de relatório desejado 
O Sistema processa os dados. 
O Sistema apresenta o relatório em tela e permite exportação em formato PDF/Excel. 

 
Fluxo Alternativo (1): Falha de geração 
Se houver inconsistência nos dados, o Sistema informa a falha e sugere nova tentativa. 

 
Pós-condições: Relatório é gerado e exibido para o Administrador. 

### 3.4.3 Diagrama de Classes 

A Figura 2 mostra o diagrama de classes do sistema. O Profissional deve conter a identificação do Cadastro e Perfil. Um Perfil pode conter um ou muitos serviços e um Servico pode estar relacionado a nenhum ou a muitos perfis. O Login deve conter a identificação de Cadastro e Administrador. 

#### Figura 2: Diagrama de Classes do Sistema.
 
![image]<img width="880" height="741" alt="Screenshot 2025-09-28 233640" src="https://github.com/user-attachments/assets/4c808724-7749-4334-9fab-755a929051e3" />



### 3.4.4 Descrições das Classes 

| # | Nome | Descrição |
|--------------------|------------------------------------|----------------------------------------|
| 1	|	Administrador  |	Cadastro de informações relativas ao administrador da plataforma |
| 2	| Login  |	Cadastro de informações de login  |
| 3 |	Profissional  |	Cadastro de todas as informações do profissional  |
| 4 |	Cadastro  | Cadastro de informações básicas do profissional |
| 5	|	Perfil  |	Cadastro de informações profissionais  |
| 6 |	Servico  |	Cadastro de informações relativas ao serviço ofertado |
