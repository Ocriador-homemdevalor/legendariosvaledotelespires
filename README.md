# Legendários — prévia HTML

Protótipo de participação gratuita em 100 números. Doações independentes não reservam números, não são requisito para participar e não aumentam as chances.

## Abrir

Abra `index.html` no navegador. Todo o visual, CSS e JavaScript estão no próprio arquivo; não é necessário instalar dependências.

## Publicar a demonstração no GitHub Pages

1. Crie um repositório no GitHub.
2. Envie os arquivos desta pasta para a raiz do repositório, incluindo `index.html` e `.nojekyll`. Não envie arquivos de participantes, comprovantes, senhas ou chaves privadas.
3. Em **Settings → Pages**, escolha **Deploy from a branch**.
4. Selecione a branch que contém os arquivos (normalmente `main`) e a pasta **/(root)**. Salve.
5. Aguarde a publicação e abra o endereço informado pelo GitHub.

Referência oficial: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

O pacote foi preparado para publicação pelo proprietário. Nenhum repositório GitHub foi criado e nenhum site GitHub Pages foi publicado nesta revisão.

## Fluxo implementado

- Pré-inscrição com nome, telefone com DDD, e-mail, cidade e UF obrigatórios.
- Endereço completo e CEP opcionais, para evitar exigir informações desnecessárias antes de um eventual contato.
- Correção dos dados antes da confirmação.
- Escolha de um número e confirmação gratuita.
- Bloqueio de telefone ou e-mail repetidos dentro da mesma sessão. Isso não verifica a identidade de uma pessoa.
- Consulta do cadastro completo no painel de demonstração.
- Simulação do sorteio entre participações confirmadas, com acesso aos contatos do contemplado.
- Lista independente de doações e comprovantes de exemplo.

## Limites importantes da prévia

Este HTML é uma demonstração, não um sistema operacional para inscrições reais. Use somente dados fictícios.

- Os dados existem apenas na memória da aba. Atualizar ou fechar a página apaga as alterações.
- Cada visitante recebe uma sessão independente. A disponibilidade dos números não é compartilhada entre visitantes ou dispositivos.
- O painel demonstrativo não possui autenticação. Ocultar um botão ou colocar uma senha no JavaScript não protegeria os dados.
- Telefone e e-mail têm validação de formato, mas não comprovação de titularidade. Não são enviados e-mails ou mensagens.
- Os comprovantes são arquivos locais temporários; não são enviados nem armazenados em um servidor.
- A simulação do sorteio pode ser reiniciada recarregando a página e não possui histórico auditável.
- A checagem de tipo e tamanho de arquivo no navegador é apenas demonstrativa; uma versão operacional precisa validá-los no servidor.

## Melhorias recomendadas antes de uso real

1. **Dados compartilhados:** conectar o HTML a um serviço de aplicação e banco de dados. A confirmação deve atribuir o número em uma operação atômica e impedir duplicidades no banco, inclusive quando duas pessoas clicarem simultaneamente.
2. **Painel protegido:** autenticar administradores e autorizar consultas no servidor. A consulta pública deve retornar apenas números e disponibilidade, nunca telefone, e-mail, endereço ou comprovantes.
3. **Contato confiável:** confirmar a titularidade do e-mail ou telefone, permitir correções por um fluxo autenticado e registrar a entrega das notificações. Enviar comprovante de participação após a confirmação real.
4. **Privacidade:** definir quem administra os dados, a finalidade, o prazo de retenção e o canal para correção/exclusão. Preferir solicitar o endereço completo apenas se necessário para entregar o prêmio. Elaborar o aviso de privacidade antes da coleta real.
5. **Regras claras:** informar prêmio, data e horário com fuso, encerramento, critérios de participação e procedimento de contato do contemplado.
6. **Resultado rastreável:** executar o sorteio no servidor, congelar a lista elegível e registrar o resultado uma única vez com data e histórico. Uma nova tentativa não deve substituir silenciosamente o resultado anterior.
7. **Operação:** backups, recuperação de falhas, limites contra abuso e testes com dispositivos distintos, inclusive duas confirmações simultâneas para o mesmo número.
8. **Doações independentes:** manter seus registros e permissões separados; jamais condicionar participação ou chances à doação. Caso haja armazenamento de comprovantes, usar acesso privado e prazo de retenção definido.

Não acrescente segredos ou cadastros pessoais ao HTML ou ao repositório público. GitHub Pages publica a interface estática; a operação compartilhada precisa de serviços externos.
