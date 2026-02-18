# Charles Proxy Firefox Exclude List

Arquivo de configuração do Charles Proxy com lista de hosts ignorados durante o monitoramento de sessões no Firefox. Reduz o ruído de chamadas de background ao gravar requisições e facilita o parser.

## O que é ignorado

Este arquivo ignora do monitoramento:

- Verificações de atualização e serviços do Firefox
- Chamadas de telemetria da Mozilla
- Serviços de CDN e addons da Mozilla
- Tráfego de reachability do Google
- Outros serviços de background que não são relevantes para a maioria dos **meus** testes

> ⛔️ **Aviso importante:
> Este arquivo pode ser agressivo demais para alguns projetos, pois exclui tráfego relacionado a serviços Mozilla essenciais. Verifique a lista de hosts após importar para garantir que não está ignorando chamadas importantes para seus testes.**

## Instalação

1. Abra o Charles Proxy
2. Acesse **Proxy > Recording Settings...**
3. Selecione a aba **Exclude**
4. Clique no botão **Import** no canto inferior esquerdo
5. Selecione o arquivo `charles-recording.xml` e clique em **Open**
6. A lista de exclusões será preenchida automaticamente
7. Clique em **OK** para salvar as configurações

## Uso

Após importar, o Charles Proxy excluirá automaticamente as requisições dos hosts configurados durante suas gravações, deixando os logs mais limpos e focados nas chamadas relevantes.
