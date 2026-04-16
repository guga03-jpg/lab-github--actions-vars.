Por que a Secret aparece no log como **? O GitHub possui um mecanismo de proteção que oculta segredos. Se ele detectar que o valor de uma secret está sendo impresso, ele substitui automaticamente por asteriscos para evitar vazamento de dados sensíveis.

O Job deploy_app consegue ler a variável BUILD_VERSION criada no Job build_app? Por quê? Não. Cada Job roda em uma máquina virtual (runner) isolada e independente. Variáveis de ambiente definidas dentro de um job não são compartilhadas com outros jobs, a menos que sejam usados outputs ou artefatos.
