[README.md](https://github.com/user-attachments/files/32962817/README.md)
# Steam Inventory Mock v3.6

Mock visual/local para o inventário CS2 no Millennium. Nenhum item Steam é criado, alterado ou enviado ao servidor.

## v3.6
- Mantém os itens falsos dentro dos slots reais da grade do inventário.
- Usa um `.item` real como modelo para preservar centralização e aparência.
- Não adiciona o nome da skin abaixo do item.
- Não força mais o `src` das imagens dos itens reais; isso evita interferir no lazy-load nativo do Steam.
- Ao clicar em uma skin falsa, não cria um painel próprio.
- O plugin abre o `inventory_iteminfo` nativo do Steam selecionando temporariamente um item real e então reescreve localmente os campos desse painel com os dados do mock.
- Atualiza tanto `iteminfo0` quanto `iteminfo1`, pois o Steam alterna esses dois painéis durante a animação/seleção.
- A seleção visual volta para o slot falso depois que o painel nativo é aberto.
- O painel nativo continua sendo o único painel de detalhes usado pelo mock.

## Build
```text
bun install
bun run build
```

O ambiente de desenvolvimento usado para gerar o ZIP não possui Bun instalado, portanto o build final deve ser executado no Windows com o Bun já utilizado para o Millennium.

## Observação
A leitura/importação de inventário de terceiros usa somente dados públicos. O mock continua sendo exclusivamente client-side.
