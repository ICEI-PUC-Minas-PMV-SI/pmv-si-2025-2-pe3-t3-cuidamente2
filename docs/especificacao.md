
# 3. DOCUMENTO DE ESPECIFICAÇÃO DE REQUISITOS DE SOFTWARE

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
| RF1 | Cadastro de Profissional |	O sistema deve permitir que Profissionais criem uma conta com login na plataforma |
| RF2 |	Edição de Dados 	| O sistema deve permitir editar dados cadastrais |
| RF3	|Atualização de Perfil   |	O sistema deve permitir que Profissionais editem um perfil profissional e solicitem validação para publicação |
| RF4 |	Estatísticas de Visualização 	| O sistema deve fornecer relatórios de visualização de perfil para o profissional, sem identificar individualmente os visitantes |
| RF5 |	Listagem de perfis 	| O sistema deve listar os Profissionais ativos e validados.  |
| RF6 |	Contato com profissional 	| O Visitante e o Administrador devem ter acesso a informações de contato para iniciar comunicação externa com o Profissional. |
| RF7 |	Administrativa 	| O Administrador deve poder editar, inativar ou reativar, validar e excluir perfis de Profissionais |
| RF8 |	Login  	| O profissional deve ter acesso ao seu perfil profissional na plataforma através de login |
| RF9 |	Linguagem e Instruções  	| O sistema deve apresentar instruções curtas, ícones e orientações visuais |
| RF10 |	Relatórios  	| O Administrador deve poder ter acesso a métricas básicas dos perfis dos profissionais e dados gerais da plataforma. |
| RF11 |Ambientes   	| O sistema deve conter um ambiente para administração e gerência dos profissionais na plataforma e outro ambiente para o Profissional gerenciar seu próprio perfil  |
| RF12 |	Tamanho de Fonte e Controle de Contraste  	| O sistema deve disponibilizar controles que permitam ao usuário ajustar o contraste e o tamanho da fonte, com pré-visualização imediata das alterações |
| RF13 |	Inclusão e Navegação   	| O sistema deve permitir navegação por teclado e ter compatibilidade com leitores de tela |

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

<img width="949" height="432" alt="image" src="https://github.com/user-attachments/assets/86d33d6d-d12c-4f70-84e2-04cae64af2b1" />


 
### 3.4.2 Descrições de Casos de Uso

### Criar Conta (CSU01) 

Sumário: O Profissional preenche o formulário para criar uma conta na plataforma (inclusão). 

Ator Primário: Profissional 

Ator Secundário: Administrador 

Pré-condições: Profissional deve ter acesso à internet e fornecer dados básicos. 

Fluxo Principal: 

O Profissional preenche o formulário inicial (Nome Completo, nº do CRP, CPF e email) para cadastrar uma conta no Sistema.  

O Profissional seleciona a operação desejada: Avançar ou opta por finalizar o caso de uso. 

 

Pós-condições: Se a operação desejada for Avançar, o Profissional receberá um email com link para criar senha de acesso ao Sistema e fazer login.  

 

### Fazer Login (CSU02) 

Sumário: O Profissional fornece dados de usuário e senha (acesso). 

Ator Primário: Profissional 

Ator Secundário:  

Pré-condições: Profissional deve ter acesso à internet e já estar cadastrado. 

Fluxo Principal: 

O Profissional preenche os campos de Usuário e Senha e solicita acesso  

O Sistema verifica a validade dos dados. Se os dados forem válidos, o Profissional acessa seu perfil. Se os dados não forem válidos, o Sistema reporta o fato e apresenta as operações que podem ser realizadas: tentar novamente ou solicitar troca de senha. 

O Profissional seleciona a operação desejada: Tentar Novamente, Solicitar Troca de Senha ou opta por finalizar o caso de uso. 

 

Fluxo Alternativo (1): Editar dados cadastrais 

O Profissional fornece o e-mail de usuário e solicita a troca de senha. 

O Sistema envia um link para o e-mail informado. 

O Profissional solicita a alteração da senha. O Sistema verifica a validade dos dados e, se eles forem válidos, altera a senha no cadastro do Profissional, caso contrário, reporta o fato. 

Pós-condições: O Profissional acessa seu perfil profissional no Sistema.
 

### Editar Perfil (CSU03)  

Sumário: O profissional deve já ter um cadastro válido no sistema. 

Ator Primário: Visitante 

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

 

Fluxo Alternativo (1): Editar dados cadastrais 

O Profissional fornece o e-mail de usuário e solicita a troca de senha. 

O Sistema envia um link para o e-mail informado. 

O Profissional solicita a alteração da senha. O Sistema verifica a validade dos dados e, se eles forem válidos, altera a senha no cadastro do Profissional, caso contrário, reporta o fato. 

Pós-condições:  


### Buscar Profissional (CSU04)  

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

 
### Gerenciar Cadastros (CSU05)  

SSumário: O Administrador fornece dados de usuário e senha (acesso). 

Ator Primário: Administrador 

Ator Secundário:  

Pré-condições: O Administrador precisa já estar cadastrado 

Fluxo Principal: 

O Administrador preenche os campos de Usuário e Senha  

 

Pós-condições:  

 

### Contactar Profissional (CSU06)  

Sumário: O Visitante inicia contato direto com um profissional. 

Ator Primário: Visitante 

Ator Secundário: Administrador 

Pré-condições: O profissional deve ter cadastro válido e perfil publicado. 

Fluxo Principal: 

O Visitante acessa o perfil de um profissional. 

O Sistema exibe os meios de contato disponíveis (WhatsApp, e-mail). 

O Visitante escolhe o meio de contato. 

O Sistema redireciona o Visitante para o aplicativo externo correspondente (WhatsApp ou e-mail). 

 

Fluxo Alternativo (1): Contato indisponível 

Caso um dos meios de contato esteja temporariamente indisponível, o Sistema notifica o visitante e sugere outra opção disponível. 

 

Pós-condições: A comunicação entre visitante e profissional é iniciada fora da plataforma. 

 
### Emitir Relatórios (CSU07)  

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

 

3.4.3 Diagrama de Classes  

A Figura 2 mostra o diagrama de classes do sistema. O Profissional deve conter a identificação do Cadastro e Perfil. Um Perfil pode conter um ou muitos serviços e um Servico pode estar relacionado a nenhum ou a muitos perfis. O Login deve conter a identificação de Cadastro e Administrador.  

### 3.4.3 Diagrama de Classes 

A Figura 2 mostra o diagrama de classes do sistema. O Profissional deve conter a identificação do Cadastro e Perfil. Um Perfil pode conter um ou muitos serviços e um Servico pode estar relacionado a nenhum ou a muitos perfis. O Login deve conter a identificação de Cadastro e Administrador. 

#### Figura 2: Diagrama de Classes do Sistema.
 
<img width="924" height="486" alt="image" src="https://github.com/user-attachments/assets/2a54f6cc-68d1-491d-88da-218eac3e338e" />




### 3.4.4 Descrições das Classes 

| # | Nome | Descrição |
|--------------------|------------------------------------|----------------------------------------|
| 1	|	Administrador  |	Cadastro de informações relativas ao administrador da plataforma |
| 2 |	Profissional  |	Cadastro de todas as informações do profissional  |
| 3 |	Servico  |	Cadastro de informações relativas ao serviço ofertado |
