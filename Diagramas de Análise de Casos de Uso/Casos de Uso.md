# Casos de uso

<h4>UC1. Cadastrar Usuário
<h4>UC2. Login
<h4>UC3. Trocar Senha
<h4>UC4. Trocar Credenciais
<h4>UC5. Buscar Professor
<h4>UC6. Buscar Componente Curricular
<h4>UC7. Solicitar Professor de Monitoria
<h4>UC8. Solicitar Professor Orientador de Estágio
<h4>UC9. Solicitar Professor Orientador de TCC
<h4>UC10. Enviar Documentos Monitoria
<h4>UC11. Enviar Documentos TCC
<h4>UC12. Enviar Documentos Estágio 
<h4>UC13. Receber Documentos
<h4>UC14. Enviar Documentos Institucionais
<h4>UC15. Solicitar Declaração de Participação Monitoria
<h4>UC16. Solicitar Declaração de Participação Estágio
<h4>UC17. Solicitar Declaração de Conclusão de Curso
<h4>UC18. Consultar Histórico de Atividades
<h4>UC19. Cadastrar Estágio (Aluno) 
<h4>UC20. Baixar documentos acadêmicos (Todos os atores do sistema) 
<h4>UC21. Acompanhar Orientações TCC (Professor)
<h4>UC22. Acompanhar Orientações Monitoria (Professor)
<h4>UC23. Acompanhar Orientações Estágio (Professor)
<h4>UC24. Avaliar Relatório Final de Monitoria (Professor e Coordenador de Monitoria)
<h4>UC25. Avaliar Relatório Final de Estágio (Professor e Coordenador de Estágio)
<h4>UC26. Avaliar TCC (Professor)
<h4>UC27. Avaliar Pedidos de Estágio (Coordenador de Estágio)
<h4>UC28. Ofertar Orientação (Professor)
<h4>UC29. Cadastrar Edital de Monitoria (Coordenador de Monitoria)
<h4>UC30. Acompanhar status estágio (Aluno, Coordenador de Estágio)
<h4>UC31. Acompanhar status monitoria (Aluno, Coordenador de Monitoria)
<h4>UC32. Consultar 'meu perfil' (Todos os atores cadastrados) </h4>

## UC1. Cadastrar Usuário

### Cenário Informal:
O caso começa quando um usuário acessa a página de cadastro do sistema e preenche o formulário com suas informações acadêmicas. Após preencher todos os campos obrigatórios, o usuário envia o formulário. O sistema valida as informações e, se estiverem corretas, cria uma nova conta para o usuário.

### Caso de Uso Primário

### Atores
- Usuário Anônimo.

### Pré-condições
- O usuário não deve ter um cadastro ativo no sistema.

### Fluxo de Eventos (caminho básico)
1. O usuário acessa a página de cadastro do sistema.
2. O sistema apresenta o formulário de cadastro com campos obrigatórios, como nome completo, endereço de e-mail e CPF.
3. O usuário preenche o formulário e envia os dados.
4. O sistema valida as informações.
5. O sistema envia um e-mail de ativação da conta.
6. O usuário confirma a criação da conta pelo e-mail de ativação.
7. A conta é criada.
8. O usuário entra na plataforma.

### Pós-condições
- O usuário é criado como Aluno ou Professor.

### Fluxo de Exceção
- No passo 4 do fluxo primário, se algum campo estiver incorreto ou incompleto, o sistema exibe uma mensagem de erro indicando quais campos necessitam de correção.

## UC2. Login

### Cenário Informal:

O caso começa quando um usuário com cadastro ativo acessa a página de login do sistema. O usuário informa seu usuário, e-mail ou CPF, e senha cadastrados. Se as credenciais estiverem corretas, o sistema autentica o usuário e o direciona para a página inicial.

### Caso de Uso Primário

### Atores

- Usuário Anônimo.

### Pré-condições

- O usuário deve possuir uma conta ativa no sistema.

### Fluxo de Eventos (caminho básico)

1. O usuário acessa a página de login.
2. O sistema apresenta os campos de usuário e senha.
3. O usuário preenche e envia as informações.
4. O sistema valida as credenciais.
5. O usuário é autenticado e direcionado para a plataforma.

### Pós-condições

- O usuário está autenticado no sistema.

### Fluxo de Exceção

- No passo 4 do fluxo primário, se as credenciais estiverem incorretas, o sistema exibe uma mensagem de erro solicitando nova tentativa.

## UC3. Trocar Senha

### Cenário Informal:

O caso começa quando um usuário não autenticado deseja alterar sua senha. O sistema solicita o endereço de e-mail cadastrado para confirmar a existência do cadastro e enviar o link para redefinição. Após abrir o link, o usuário informa a nova senh que será armazenada no sistema.

### Caso de Uso Primário

### Atores

- Usuário Anônimo

### Pré-condições

- O usuário deve estar cadastrado no sistema.
- O usuário não deve estar autenticado no sistema.

### Fluxo de Eventos (caminho básico)

1. O usuário acessa a página de login.
2. O usuário seleciona a opção de trocar senha.
3. O usuário informa seu endereço de e-mail cadastrado.
4. O sistema valida o endereço de e-mail.
5. O sistema envia por e-mail um link para redefinição da senha.
6. O usuário confirma a solicitação de mudança de senha pelo link de redefinição recebido no e-mail.
7. O usuário informa a nova senha.
8. O sistema valida a informação.
9. O sistema atualiza as credenciais do usuário.

### Pós-condições

- As credenciais do usuário são atualizadas com sucesso.
- O usuário é desconectado de todos os dispositivos conectados previamente.

### Fluxo de Exceção

- No passo 4 do fluxo primário, se o endereço de e-mail não estiver cadastrado, o sistema exibe mensagem de erro.

## UC4. Trocar Credenciais

### Cenário Informal

O caso começa quando um usuário autenticado deseja alterar seu e-mail ou senha. O sistema solicita as credenciais atuais para confirmar a identidade. Após validação, o usuário informa os novos dados, que são atualizados no sistema.

### Caso de Uso Primário

### Atores

- Aluno.
- Monitor.
- Estagiário.
- Autor de TCC.
- Professor.

### Pré-condições

- O usuário deve estar autenticado no sistema.

### Fluxo de Eventos (caminho básico)

1. O usuário acessa a área de configurações de conta.
2. O sistema apresenta as opções para alterar e-mail ou senha.
3. O usuário seleciona uma das opções.
4. O sistema envia por e-mail um link para redefinição da credencial escolhida.
5. O usuário informa a credencial atual e a nova.
6. O sistema valida as informações.
7. O sistema atualiza as credenciais do usuário.

### Pós-condições

- As credenciais do usuário são atualizadas com sucesso.
- O usuário é desconectado de todos os dispositivos conectados previamente.

### Fluxo de Exceção

- No passo 6 do fluxo primário, se as credenciais atuais estiverem incorretas ou os novos dados forem inválidos, o sistema exibe mensagem de erro.

## UC5. Buscar Professor

### Cenário Informal:

O caso começa quando um usuário autenticado deseja buscar informações sobre um professor cadastrado na plataforma. O usuário acessa a página de busca, insere as informações de busca e visualiza os resultados.

### Caso de Uso Primário

### Atores

- Aluno.
- Monitor.
- Estagiário.
- Autor de TCC.
- Coordenador de Monitorias.
- Coodenador de Estágio.

### Pré-condições

- O usuário deve estar autenticado no sistema.

### Fluxo de Eventos (caminho básico)

1. O usuário acessa a página de busca de professores.
2. O sistema apresenta o formulário de busca.
3. O usuário preenche os critérios de busca.
4. O sistema busca os professores correspondentes e exibe os resultados.

### Pós-condições

- A lista de professores é apresentada ao usuário.

### Fluxo de Exceção

- No passo 4 do fluxo primário, se não houver professores correspondentes, o sistema exibe uma mensagem informando que não foram encontrados resultados.

## UC6. Buscar Componente Curricular

### Cenário Informal:

O caso começa quando um aluno autenticado deseja consultar os componentes curriculares disponíveis. O aluno acessa a página de busca, informa filtros ou palavras-chave e visualiza os componentes listados.

### Caso de Uso Primário

### Atores

- Aluno.

### Pré-condições

- O aluno deve estar autenticado no sistema.

### Fluxo de Eventos (caminho básico)

1. O aluno acessa a página de busca de componentes curriculares.
2. O sistema apresenta o formulário de busca.
3. O aluno preenche os filtros ou termos de busca e envia.
4. O sistema busca os componentes curriculares correspondentes e exibe os resultados.

### Pós-condições

- A lista de componentes curriculares é apresentada ao aluno.

### Fluxo de Exceção

- No passo 4 do fluxo primário, se não houver componentes correspondentes, o sistema informa que não foram encontrados resultados.

## UC7. Solicitar Professor de Monitoria

### Cenário Informal:

O caso começa quando um aluno deseja solicitar um professor para monitoria em um componente curricular. O aluno seleciona o componente e escolhe um professor disponível, enviando a solicitação.

### Caso de Uso Primário

### Atores

- Aluno.
- Estagiário.
- Autor de TCC.

### Pré-condições

- O usuário deve estar autenticado no sistema.
- O usuário não pode ser Monitor.

### Fluxo de Eventos (caminho básico)

1. O aluno acessa a página de solicitações de monitoria.
2. O sistema exibe os componentes disponíveis e os professores relacionados.
3. O aluno escolhe o professor e envia a solicitação.
4. O sistema registra a solicitação de monitoria.

### Pós-condições

- A solicitação de monitoria é criada no sistema.

### Fluxo de Exceção

- No passo 3 do fluxo primário, se não houver professores disponíveis para o componente, o sistema exibe uma mensagem de aviso.

## UC8. Solicitar Professor Orientador de Estágio

### Cenário Informal:

O caso começa quando um aluno deseja solicitar um professor para orientação de estágio. O aluno escolhe um professor da lista e envia a solicitação.

### Caso de Uso Primário

### Atores

- Aluno.
- Monitor.
- Autor de TCC.

### Pré-condições

- O usuário deve estar autenticado no sistema.
- O usuário não pode ser Estagiário.

### Fluxo de Eventos (caminho básico)

1. O aluno acessa a área de solicitação de orientação de estágio. 
2. O sistema exibe a lista de professores disponíveis.
3. O aluno seleciona um professor e envia a solicitação.
4. O sistema registra a solicitação de orientação.

### Pós-condições

- A solicitação de orientação de estágio é criada no sistema.

### Fluxo de Exceção

- No passo 2 do fluxo primário, se não houver professores disponíveis, o sistema exibe uma mensagem informativa.

## UC9. Solicitar Professor Orientador de TCC

### Cenário Informal:

O caso começa quando um aluno deseja solicitar um professor para orientação de TCC (Trabalho de Conclusão de Curso). O aluno acessa a área de solicitação, seleciona um professor e formaliza a solicitação.

### Caso de Uso Primário

### Atores

- Aluno.

### Pré-condições

- O usuário deve estar autenticado no sistema.
- O usuário não pode ser Autor de TCC.

### Fluxo de Eventos (caminho básico)

1. O aluno acessa a área de solicitação de orientação de TCC. 
2. O sistema exibe a lista de professores disponíveis.
3. O aluno seleciona um professor e envia a solicitação.
4. O sistema registra a solicitação de orientação.

### Pós-condições

- A solicitação de orientação de TCC é criada no sistema.

### Fluxo de Exceção

- No passo 2 do fluxo primário, se não houver professores disponíveis, o sistema exibe uma mensagem informativa.

## UC10. Enviar Documentos Monitoria

### Cenário Informal:

O caso começa quando o Monitor acessa a área de envio de documentos de Monitoria. Ele seleciona o tipo de documento (relatório, ficha de frequência, etc.), anexa o arquivo e confirma o envio. O sistema valida o tipo e formato do arquivo e armazena o documento associado à atividade de monitoria.

### Caso de Uso Primário:

### Atores:

- Monitor.

### Pré-condições:

- O monitor deve estar logado no sistema e vinculado a uma atividade de monitoria ativa.

### Fluxo de Eventos (caminho básico):

1. O monitor acessa a área de envio de documentos da monitoria.
2. O sistema apresenta as opções de tipos de documentos aceitos.
3. O monitor seleciona o tipo de documento e faz o upload do arquivo.
4. O sistema valida o arquivo (formato, tamanho).
5. O sistema confirma o recebimento do documento.
6. O documento é armazenado no sistema e vinculado à atividade do monitor.

### Pós-condições:

- O documento é registrado no histórico de atividades da monitoria.

### Fluxo de Exceção:

- No passo 4, se o arquivo enviado for inválido, o sistema exibe uma mensagem de erro indicando o problema.

## UC11. Enviar Documentos TCC

### Cenário Informal:

O Autor de TCC acessa o ambiente de submissão de documentos de TCC, escolhe o tipo de documento (projeto, monografia, versão final, etc.), anexa o arquivo e confirma o envio. O sistema verifica o formato e registra o documento para a orientação correspondente.

### Caso de Uso Primário:

### Atores:

- Autor de TCC.

### Pré-condições:

- O aluno deve estar cadastrado como Autor de TCC e ter vínculo com um orientador.

### Fluxo de Eventos (caminho básico):

1. O autor de TCC acessa a área de envio de documentos.
2. O sistema apresenta os tipos de documentos aceitos.
3. O autor seleciona o tipo de documento e faz o upload.
4. O sistema valida o arquivo (formato, tamanho).
5. O sistema armazena o documento no sistema e associa ao projeto de TCC.
6. O sistema notifica o professor orientador.

### Pós-condições:

- O documento é associado ao projeto de TCC em andamento.

### Fluxo de Exceção:

- No passo 4, caso o documento esteja em formato inválido, o sistema rejeita o envio e informa o erro.

## UC12. Enviar Documentos Estágio

### Cenário Informal:

O Estagiário acessa a área de envio de documentos de estágio, escolhe o tipo de documento (termo de compromisso, relatório parcial, relatório final), anexa o arquivo e confirma o envio. O sistema valida os dados e registra a submissão no processo de estágio.

### Caso de Uso Primário:

### Atores:

- Estagiário.

### Pré-condições:

- O estagiário deve ter um estágio cadastrado e ativo no sistema.

### Fluxo de Eventos (caminho básico):

1. O estagiário acessa a seção de envio de documentos.
2. O sistema apresenta os tipos de documentos aceitos.
3. O estagiário escolhe o tipo e anexa o arquivo.
4. O sistema valida o arquivo.
5. O sistema confirma e registra o documento no processo de estágio.

### Pós-condições:

- O documento é registrado e disponível para análise dos responsáveis.

### Fluxo de Exceção:

- No passo 4, documentos inválidos são rejeitados e o estagiário é notificado do erro.

## UC13. Receber Documentos

### Cenário Informal:

O ator acessa a área de recebimento de documentos para consultar ou baixar arquivos enviados a ele no âmbito da atividade acadêmica (monitoria, estágio ou TCC).

### Caso de Uso Primário:

### Atores:

- Aluno.
- Professor.
- Monitor.
- Autor de TCC.
- Estagiário.

### Pré-condições:

- O usuário deve estar logado no sistema e possuir documentos disponíveis.

### Fluxo de Eventos (caminho básico):

1. O usuário acessa a seção de documentos recebidos.
2. O sistema lista os documentos disponíveis.
3. O usuário seleciona o documento desejado.
4. O sistema disponibiliza o download ou visualização do documento.

### Pós-condições:

- O documento é acessado ou baixado pelo usuário.

### Fluxo de Exceção:

- Se não houver documentos disponíveis, o sistema informa ao usuário.

## UC14. Enviar Documentos Institucionais

### Cenário Informal:

O ator (professor ou coordenador) acessa a área de envio de documentos institucionais para anexar editais, regulamentos ou certificados, enviando-os para alunos ou setores.

### Caso de Uso Primário:

### Atores:

- Professor.
- Coordenador de Monitoria.
- Coordenador de Estágio.

### Pré-condições:

- O ator deve possuir permissão para envio institucional.

### Fluxo de Eventos (caminho básico):

1. O ator acessa a seção de envio institucional.
2. O sistema exibe os tipos de documentos aceitos.
3. O ator seleciona o tipo e envia o arquivo.
4. O sistema valida e registra o documento.

### Pós-condições:

- O documento é publicado para os destinatários previstos.

### Fluxo de Exceção:

- Arquivos fora do padrão são rejeitados com aviso de erro.

## UC15. Solicitar Declaração de Participação Monitoria

### Cenário Informal:

O aluno que participou de uma atividade de monitoria acessa a área de solicitações e requisita a emissão da declaração de participação.

### Caso de Uso Primário:

### Atores:

- Aluno.

### Pré-condições:

- O aluno deve ter concluído a atividade de monitoria.

### Fluxo de Eventos (caminho básico):

1. O aluno acessa a seção de solicitações.
2. O aluno seleciona "Solicitar Declaração de Monitoria".
3. O sistema gera a declaração e disponibiliza para o aluno.

### Pós-condições:

- A declaração de participação é emitida e disponível para download.

### Fluxo de Exceção:

- Se a participação não estiver finalizada, o sistema não libera a emissão.

## UC16. Solicitar Declaração de Participação Estágio

### Cenário Informal:

O aluno que completou seu estágio acessa a área de solicitações e pede a emissão da declaração de participação no estágio.

### Caso de Uso Primário:

### Atores:

- Aluno.

### Pré-condições:

- O aluno deve ter um estágio registrado como concluído.

### Fluxo de Eventos (caminho básico):

1. O aluno acessa a área de solicitações.
2. Seleciona "Solicitar Declaração de Estágio".
3. O sistema gera e disponibiliza a declaração.

### Pós-condições:

- A declaração é emitida para o aluno.

### Fluxo de Exceção:

- Caso o estágio não esteja finalizado, o sistema impede a emissão.

## UC17. Solicitar Declaração de Conclusão de Curso

### Cenário Informal:

Após a conclusão do TCC, o aluno solicita ao sistema a emissão da declaração de conclusão do curso.

### Caso de Uso Primário:

### Atores:

- Aluno.

### Pré-condições:

- O aluno deve ter aprovado o TCC e finalizado os trâmites do curso.

### Fluxo de Eventos (caminho básico):

1. O aluno acessa a seção de solicitações.
2. Seleciona "Solicitar Declaração de Conclusão de Curso".
3. O sistema valida as condições e gera a declaração.

### Pós-condições:

- A declaração de conclusão de curso é emitida.

### Fluxo de Exceção:

- Se o aluno não atender aos critérios de conclusão, a solicitação é recusada.

## UC18. Consultar Histórico de Atividades

### Cenário Informal:

O usuário acessa o sistema para visualizar todo o histórico de suas atividades acadêmicas, como monitorias, estágios e projetos de TCC.

### Caso de Uso Primário:

### Atores:

- Aluno.
- Monitor.
- Estagiário.
- Autor de TCC.
- Professor.
- Coordenador de Monitorias.
- Coodenador de Estágio.

### Pré-condições:

- O usuário deve estar autenticado no sistema.

### Fluxo de Eventos (caminho básico):

1. O usuário acessa seu perfil.
2. O sistema apresenta a seção "Histórico de Atividades".
3. O usuário visualiza as atividades realizadas.

### Pós-condições:

- O usuário consulta seu histórico completo.

### Fluxo de Exceção:

- Se não houver atividades registradas, o sistema informa o usuário.

## UC19. Cadastrar Estágio

### Cenário Informal:

O caso começa quando um aluno precisa registrar um novo estágio no sistema para validação institucional.

### Atores
- Aluno

### Pré-condições
- Ter completado 50% da carga horária do curso
- Não ter estágios ativos em paralelo

### Fluxo de Eventos (caminho básico)
1. Acessa "Estágios > Novo Cadastro"
2. Preenche formulário com:
   - Dados da empresa (CNPJ válido)
   - Plano de atividades
   - Período previsto
3. Anexa documentação comprobatória
4. Submete para análise
5. O sistema envia para aprovação do coordenador

### Pós-condições
- Estágio aparece como "Pendente de Aprovação"
- Aluno recebe confirmação de recebimento

### Fluxo de Exceção
- No passo 2, se CNPJ for inválido, o sistema bloqueia envio
- No passo 3, se faltar documento obrigatório, o sistema lista itens faltantes

## UC20. Baixar Documentos Acadêmicos

### Cenário Informal:
O caso começa quando qualquer usuário autenticado precisa baixar documentos oficiais disponíveis no sistema.

### Atores
- Todos os usuários do sistema

### Pré-condições
- Ter permissão de acesso ao documento

### Fluxo de Eventos (caminho básico)
1. O usuário acessa "Documentos"
2. Seleciona categoria desejada:
   - Modelos
   - Editais
   - Documentos Pessoais
3. Aplica filtros de busca
4. Seleciona documento
5. Clica em "Download"
6. O sistema registra o acesso

### Pós-condições
- Documento salvo localmente
- Registro de download no sistema

### Fluxo de Exceção
- No passo 4, se o documento estiver restrito, o sistema solicita justificativa de acesso
- No passo 5, se o arquivo estiver corrompido, o sistema gera novo link de download

## UC21. Acompanhar Orientações de TCC

### Cenário Informal:
O caso começa quando um professor orientador deseja acompanhar o progresso dos seus orientandos de TCC.

### Atores
- Professor

### Pré-condições
- Ter pelo menos um orientando ativo

### Fluxo de Eventos (caminho básico)
1. Acessa "Orientações > TCC"
2. O sistema lista todos os orientandos
3. Seleciona um orientando
4. Visualiza:
   - Entregas realizadas
   - Prazos
   - Histórico de feedbacks
5. Registra novas observações

### Pós-condições
- As novas observações ficam disponíveis para o aluno orientado.
- O sistema atualiza o status do progresso do TCC.

### Fluxo de Exceção
- EA1: Se no passo 2 não houver orientandos:
   - O sistema exibe uma mensagem informando a ausência de orientandos.
   - O sistema sugere que o professor cadastre disponibilidade para orientar novos alunos
- EA2: Se no passo 4 houverem atrasos:
   - O sistema destaca as informações de prazos em vermelho para alertar o professor.

## UC22. Acompanhar Orientações de Monitoria

### Cenário Informal:

O professor responsável deseja acompanhar o desempenho dos monitores que estão sob sua supervisão. O sistema consolida todas as informações relevantes em um painel único.

### Atores
- Professor

### Pré-condições
- Ter sido designado como professor responsável por, pelo menos, uma disciplina
- Ter pelo menos um monitor ativo

### Fluxo de Eventos (caminho básico)
1. O professor acessa "Monitorias > Acompanhamento"
2. O sistema exibe lista de monitores vinculados
3. Seleciona um monitor específico
4. O sistema exibe:
   - Horas cumpridas
   - Relatórios entregues
   - Avaliações anteriores
   - Próximos prazos
5. Registra feedback ou orientações

### Pós-condições
- O registro de acompanhamento é armazenado
- O histórico da monitoria é atualizado
- O sistema notifica o(s) monitor(es) sobre as observações

### Fluxo de Exceção

- EA1: No passo 2, se não houver monitores ativos:
   - O sistema notifica o professor
   - O sistema sugere convocação de novos monitores
- EA2: No passo 4, se houver atrasos críticos:
   - O sistema alerta automaticamente o coordenador de monitoria por e-mail ou notificação interna 

## UC23. Acompanhar Orientações de Estágio

### Cenário Informal:

O professor orientador deseja acompanhar o progresso dos estagiários sob sua responsabilidade. O sistema oferece uma visão consolidada dos dados acadêmicos e avaliações de campo, permitindo intervenções e acompanhamento eficaz.

### Atores
- Professor

### Pré-condições
- Ter sido designado como professor orientador de estágio
- Ter pelo menos um estagiário ativo sob sua responsabilidade

### Fluxo de Eventos (caminho básico)
1. O professor acessa "Estágios > Orientação"
2. O sistema lista todos os estagiários vinculados
3. Seleciona um estagiário específico
4. O sistema exibe:
   - Plano de atividades
   - Relatórios entregues
   - Avaliações da empresa
   - Cumprimento de carga horária
5. Preenche avaliação parcial ou final

### Pós-condições

- As avaliações (parciais ou finais) ficam disponíveis para o estagiário e o coordenado
- O sistema salva as avaliações e calcula automaticamente o progresso total do estágio
- O estagiário é notificado das alterações feitas pelo professor

### Fluxo de Exceção

- EA1: No passo 4, se houver divergência na carga horária:
   - O sistema sugere auditoria
   - O sistema notifica o coordenador de estágio e o aluno via email ou notificação interna

- EA2: No passo 5, se a avaliação for negativa: 
   - O sistema gera plano de correção automático
   - O sistema notifica o coordenador de estágio e o estagiário via email ou notificação interna 

## UC24. Avaliar Relatório Final de Monitoria

### Cenário Informal:
O caso começa quando um professor ou coordenador recebe um relatório final de monitoria para avaliação. O sistema fornece instrumentos de avaliação padronizados.

### Atores
- Professor
- Coordenador de Monitoria

### Pré-condições
- Ter recebido relatório final para avaliação
- Estar dentro do prazo de avaliação

### Fluxo de Eventos (caminho básico)
1. O avaliador acessa "Avaliações > Monitoria"
2. O sistema exibe relatórios pendentes
3. Seleciona o relatório a avaliar
4. Preenche formulário de avaliação com:
   - Notas por critério
   - Comentários específicos
   - Recomendações
5. Submete a avaliação
6. O sistema registra e notifica o monitor

### Pós-condições
- O resultado da avaliação é vinculado ao histórico do monitor
- O status da monitoria é atualizado

### Fluxo de Exceção
- No passo 4, se o relatório for insuficiente, o sistema permite solicitar revisão
- No passo 5, se ultrapassar o prazo, o sistema notifica a coordenação

## UC25. Avaliar Relatório Final de Estágio

### Cenário Informal:
O caso começa quando um professor ou coordenador precisa avaliar um relatório final de estágio. O sistema oferece checklist completo dos requisitos.

### Atores
- Professor
- Coordenador de Estágio

### Pré-condições
- Relatório final submetido pelo estagiário
- Documentação complementar completa

### Fluxo de Eventos (caminho básico)
1. O avaliador acessa "Avaliações > Estágio"
2. O sistema lista relatórios recebidos
3. Seleciona relatório específico
4. Analisa documento anexo
5. Verifica conformidade com:
   - Formatação padrão
   - Conteúdo mínimo obrigatório
   - Assinaturas digitais
6. Registra avaliação no sistema
7. O sistema atualiza o status do estágio

### Pós-condições
- O resultado é comunicado ao estagiário e empresa conveniada
- O histórico acadêmico é atualizado

### Fluxo de Exceção
- No passo 5, se faltar item obrigatório, o sistema gera termo de devolução
- No passo 6, se houver inconsistência grave, o sistema alerta a comissão de estágios

## UC26. Avaliar TCC

### Cenário Informal:
O caso começa quando um professor orientador recebe um Trabalho de Conclusão de Curso submetido por seu orientando para avaliação final. O sistema disponibiliza ferramentas para análise completa do trabalho.

### Atores
- Professor (Orientador)

### Pré-condições
- Ter vínculo ativo como orientador do TCC
- O trabalho deve estar na fase final de avaliação
- Todos os capítulos devem ter sido aprovados nas etapas anteriores

### Fluxo de Eventos (caminho básico)
1. O professor recebe notificação do sistema sobre TCC pronto para avaliação
2. Acessa a área "Avaliação de TCC"
3. O sistema exibe:
   - Versão completa do trabalho
   - Histórico de entregas anteriores
   - Pareceres dos co-orientadores (se aplicável)
4. Realiza avaliação utilizando o formulário padronizado:
   - Nota por critério (conteúdo, formatação, originalidade)
   - Comentários específicos por capítulo
   - Recomendações para publicação
5. Submete a avaliação completa
6. O sistema registra o resultado e notifica:
   - O aluno autor
   - A banca examinadora
   - A coordenação do curso

### Pós-condições
- O TCC recebe status "Aprovado" ou "Reprovado"
- O resultado final é registrado no histórico acadêmico
- Geração automática da ata de defesa (para TCCs aprovados)

### Fluxo de Exceção
- No passo 4, se o trabalho for reprovado:
  - O sistema gera termo de correções
  - Estabelece novo prazo para reapresentação
  - Notifica a coordenação sobre a reprovação
- No passo 5, se houver divergência entre orientador e co-orientador:
  - O sistema encaminha para comitê avaliador
  - Suspende o prazo de avaliação

## UC27. Avaliar Pedidos de Estágio

### Cenário Informal:
O caso começa quando o coordenador de estágio precisa analisar e aprovar novas solicitações de estágio dos alunos.

### Atores
- Coordenador de Estágio

### Pré-condições
- Ter solicitações pendentes no sistema
- Estar dentro do período letivo válido

### Fluxo de Eventos (caminho básico)
1. O coordenador acessa "Estágios > Solicitações"
2. O sistema lista pedidos pendentes
3. Seleciona um pedido específico
4. Analisa:
   - Documentação da empresa
   - Plano de atividades
   - Adequação ao curso
5. Aprova ou reprova com justificativa
6. O sistema notifica o aluno e orientador

### Pós-condições
- O estágio aparece como "Aprovado" ou "Reprovado"
- O sistema gera termo de aceite quando aplicável

### Fluxo de Exceção
- No passo 4, se a empresa não for conveniada, o sistema inicia fluxo de conveniamento
- No passo 5, se reprovado, o sistema sugere alternativas ao aluno

## UC28. Ofertar Orientação

### Cenário Informal:

Um professor deseja disponibilizar vagas para orientação de Trabalhos de Conclusão de Curso (TCC) ou estágios. O sistema permite que o docente configure requisitos e parâmetros da oferta, tornando-a visível a alunos qualificados e aptos a solicitá-la.

### Atores
- Professor

### Pré-condições
- Ter cadastro ativo como orientador
- Não ter atingido o limite máximo de orientandos

### Fluxo de Eventos (caminho básico)
1. O professor acessa "Orientações > Ofertar"
2. Seleciona tipo de orientação: TCC ou Estágio
3. Define os parametros da oferta:
   - Áreas de interesse
   - Vagas disponíveis
   - Requisitos mínimos
   - Período de disponibilidade
4. Publica a oferta

### Pós-condições
- A oferta torna-se visível apenas para alunos que atendam aos critérios definidos
- O professor passa a receber solicitações de orientação por meio do sistema
- A oferta do professor é listada na vitrine de orientações

### Fluxo de Exceção

- EA1: No passo 1, caso o professor não tenha cadastro como orientador:
   - O sistema notifica o professor com uma mensagem
   - O sistema bloqueia a tentativa e retorna para a página de início

- EA2: No passo 2, caso o professor tenha exceda o número máximo de orientandos da modalidade escolhida:
   - O sistema notifica o professor com uma mensagem
   - O sistema bloqueia a tentativa e retorna para a página de início

- EA3: No passo 3, se houver extrapolamento da carga horária máxima:
   - O sistema notifica o professor com uma mensagem
   - O sistema impede a publicação da oferta


## UC29. Cadastrar Edital de Monitoria

### Cenário Informal:
O caso começa quando o Coordenador de Monitoria precisa criar um novo edital para seleção de monitores. O sistema oferece formulário padronizado com todos os elementos obrigatórios.

### Atores
- Coordenador de Monitoria

### Pré-condições
- Ter permissão de coordenação ativa
- Estar no período de planejamento acadêmico
- Ter as disciplinas elegíveis definidas

### Fluxo de Eventos (caminho básico)
1. O coordenador acessa "Editais > Novo Edital"
2. O sistema exibe formulário com:
   - Campos obrigatórios (número, período vigente)
   - Disciplinas disponíveis
   - Modelos pré-aprovados
3. Preenche os dados do edital:
   - Vagas por disciplina
   - Requisitos acadêmicos
   - Cronograma completo
   - Documentos necessários
4. Anexa documentos complementares
5. O sistema valida a completude das informações
6. Publica o edital no sistema
7. Dispara notificações para:
   - Alunos elegíveis
   - Professores responsáveis
   - Secretaria acadêmica

### Pós-condições
- O edital fica disponível no mural oficial
- Geração automática da página de inscrições
- Criação de processos seletivos associados

### Fluxo de Exceção
- No passo 3, se houver conflito com editais anteriores:
  - O sistema alerta sobre sobreposições
  - Sugere ajustes nas datas
- No passo 5, se faltar informação essencial:
  - O sistema destaca os campos incompletos
  - Impede a publicação até a correção
- No passo 6, se publicar fora do período ideal:
  - O sistema requer justificativa formal
  - Notifica a diretoria acadêmica

## UC30. Acompanhar Status de Estágio

### Cenário Informal:

O caso começa quando um aluno estagiário ou coordenador de estágio acessa o sistema para verificar o andamento das atividades de estágio, incluindo progresso, pendências e avaliações.  

### Atores
- Aluno (Estagiário)  
- Coordenador de Estágio  

### Pré-condições
- O estágio deve estar cadastrado e aprovado no sistema
- O usuário deve ter permissões de acesso (aluno vinculado ao estágio ou coordenador de estágio) 

### Fluxo de Eventos (caminho básico)
1. O usuário acessa a seção "Estágios > Acompanhamento".  
2. O sistema exibe:  
   - Progresso atual (horas cumpridas/total).  
   - Relatórios entregues e seus status.  
   - Avaliações do orientador e da empresa (se aplicável).  
   - Próximos prazos importantes.  
3. O usuário seleciona "Detalhes".
4. O sistema exibe:  
   - Feedback detalhado do orientador.  
   - Histórico completo de atividades.  
   - Documentos vinculados.  

### Pós-condições
- O sistema registra a consulta no histórico de acesso do usuário.  

### Fluxo de Exceção
- EA1: No passo 2, se o estágio não estiver cadastrado:  
   - O sistema exibe notificação informando que não há estágio vinculado ao usuário
- EA2: No passo 4, se houver dados inconsistentes: 
   - O sistema exibe um alerta 
   - O sistema notifica a coordenação para verificação manual.

## UC31. Acompanhar Status de Monitoria

### Cenário Informal:

O caso começa quando um monitor ou coordenador deseja verificar o andamento atual das atividades de monitoria.

### Atores
- Aluno (Monitor)
- Coordenador de Monitoria

### Pré-condições
- O usuário deve ter permissões de acesso (aluno vinculado a uma monitoria ou coordenador de estágio) 
   
### Fluxo de Eventos (caminho básico)
1. O usuário acessa "Monitoria > Andamento"
2. O sistema exibe:
   - Progresso atual
   - Próximas entregas
   - Pendências
   - Histórico de avaliações
3. O usuário seleciona item específico para visualizar os detalhes
4. O sistema exibe um relatório completo do item selecionado

### Pós-condições
- O sistema registra a consulta no histórico de acessos
- Alertas e notificações são atualizadas, se necessário

### Fluxo de Exceção

- EA1:No passo 2, se houver irregularidades:
   - O sistema destaca em vermelho os itens irregulares

- EA2:No passo 3, se o monitor estiver inativo:
   - O sistema exibe um alerta ao monitor
   - O sistema notifica o coordenador de monitoria 

## UC32. Consultar 'Meu Perfil'

### Cenário Informal:

O caso começa um usuário autenticado acessa o sistema para visualizar suas informações pessoais, acadêmicas e atividades vinculadas.  

### Atores 
- Aluno  
- Monitor  
- Estagiário  
- Autor de TCC  
- Professor  
- Coordenador de Monitoria  
- Coordenador de Estágio  

### Pré-condições
- O usuário deve estar autenticado no sistema.  

### Fluxo de Eventos (caminho básico)
1. O usuário clica em "Meu Perfil" no menu principal.  
2. O sistema exibe as seguintes seções:  
   - Dados Pessoais: Nome, CPF, e-mail institucional.  
   - Informações Acadêmicas: Curso, matrícula, período (para alunos) ou departamento (para docentes).  
   - Atividades Vinculadas:
     Monitorias/Estágios em andamento (para alunos)
     Orientações ativas (para professores)
     Editais publicados (para coordenadores)
   - Configurações de Conta.
3. O usuário navega entre as seções para ver detalhes.  

### Pós-condições
- O usuário pode verificar a precisão de suas informações cadastrais.  
- O sistema registra o acesso ao perfil.  

### Fluxo de Exceção
- EA1: No passo 2, se os dados estiverem desatualizados:  
   - O sistema notifica o usuário sobre a necessidade de atualização dos dados 
- EA2: No passo 2, se não houver atividades vinculadas:  
   - O sistema recomenda as atividades disponíveis de acordo com as permissões do usuário 

