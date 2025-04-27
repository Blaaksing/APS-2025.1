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
<h4>UC32. Consultar 'meu perfil' (Todos os atores cadastrados)</h4>

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

- Aluno.
- Monitor.
- Estagiário.
- Autor de TCC.
- Professor.
- Coordenador de Monitorias.
- Coordenador de Estágio.

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

- Aluno.
- Monitor.
- Estagiário.
- Autor de TCC.
- Professor.

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
- Professor.
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

