# Casos de uso

1. Cadastrar Usuário
2. Login
3. Trocar Senha
4. Trocar Credenciais
5. Buscar Professor
6. Buscar Componente Curricular
7. Solicitar Professor de Monitoria
8. Solicitar Professor Orientador de Estágio
9. Solicitar Professor Orientador de TCC
10. Enviar Documentos Monitoria (Monitor)
11. Enviar Documentos TCC (Autor de TCC)
12. Enviar Documentos Estágio (Estagiário) 
13. Receber Documentos (Aluno, Professor, Monitor, Autor de TCC, Estagiário)
14. Enviar Documentos Institucionais (Professor, Coordenador de Monitoria e Coordenador de Estágio)
15. Solicitar Declaração de Participação Monitoria (Aluno)
16. Solicitar Declaração de Participação Estágio (Aluno)
17. Solicitar Declaração de Conclusão de Curso (Aluno)
18. Consultar Histórico de Atividades (Todos os atores cadastrados)
19. Cadastrar Estágio (Aluno)
20. Baixar documentos acadêmicos (Todos os atores do sistema)
21. Acompanhar Orientações TCC (Professor) 
22. Acompanhar Orientações Monitoria (Professor)
23. Acompanhar Orientações Estágio (Professor)
24. Avaliar Relatório Final de Monitoria (Professor e Coordenador de Monitoria)
25. Avaliar Relatório Final de Estágio (Professor e Coordenador de Estágio)
26. Avaliar TCC (Professor)
27. Avaliar Pedidos de Estágio (Coordenador de Estágio)
28. Ofertar Orientação (Professor)
29. Cadastrar Edital de Monitoria (Coordenador de Monitoria)
30. Acompanhar status estágio (Aluno, Coordenador de Estágio)
31. Acompanhar status monitoria (Aluno, Coordenador de Monitoria)
32. Consultar 'meu perfil' (Todos os atores cadastrados)

## 1. Cadastrar Usuário

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

## 2. Login

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

## 3. Trocar Senha

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

## 4. Trocar Credenciais

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

## 5. Buscar Professor

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

## 6. Buscar Componente Curricular

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

## 7. Solicitar Professor de Monitoria

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

## 8. Solicitar Professor Orientador de Estágio

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

## 9. Solicitar Professor Orientador de TCC

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