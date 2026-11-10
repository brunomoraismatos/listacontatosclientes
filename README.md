# Contatos por conta

Consulta interna dos contatos de cada conta, por Platform Account ID ou Subscription ID, no layout Tangram (RD Station).

A página é um único arquivo estático (`index.html`). A base de contatos vai embutida e **criptografada** (AES-256-GCM, chave derivada de usuário + senha com PBKDF2-SHA256, 600 mil iterações). A senha não está gravada no arquivo nem neste repositório: sem ela, os dados não podem ser lidos.

## Publicar no GitHub Pages

1. Envie `index.html` e este `README.md` para a raiz do repositório, na branch `main`.
2. Em **Settings → Pages**, escolha **Deploy from a branch**, branch `main`, pasta `/ (root)`, e salve.
3. Em um ou dois minutos o endereço aparece no topo da mesma tela: `https://<usuario>.github.io/<repositorio>/`.

## Base de dados

- Origem: export do BigQuery de 10/11/2026, 17:42.
- 85.393 contas, 103.613 assinaturas e 538.331 contatos.
- Para atualizar, gere um novo export e gere um novo `index.html` com ele. Substitua o arquivo no repositório.

## Segurança

- Nunca coloque a senha neste repositório, em issues, em commits ou no README.
- Envie o link e a senha por canais diferentes.
- Ao trocar a senha, gere um novo `index.html` e substitua o antigo. Cópias antigas do arquivo continuam abrindo com a senha antiga.
- O GitHub guarda o histórico: um arquivo antigo continua acessível pelos commits anteriores. Para revogar de verdade, apague e recrie o repositório.
- A página tem `noindex`, para não aparecer em buscadores.
