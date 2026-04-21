# Bibliocodes Cutter PHA

## Visão geral

Projeto simples com páginas HTML e tabelas JSON usadas para visualizar e pesquisar códigos Cutter e PHA.

Este repositório contém páginas estáticas que leem JSON locais para apresentar tabelas e uma interface de busca.

## Estrutura do projeto

- `index.html` — Página inicial (ponto de entrada).
- `search.html` — Interface de busca por termos/códigos.
- `cutter_table.html` — Visualiza a tabela Cutter.
- `pha_table.html` — Visualiza a tabela PHA.
- `tabela_cutter.json` — Dados principais da tabela Cutter (máquina legível).
- `tabela_cutter_leitura.json` — Versão para leitura humana da tabela Cutter.
- `tabela_pha.json` — Dados principais da tabela PHA (máquina legível).
- `tabela_pha_leitura.json` — Versão para leitura humana da tabela PHA.
- `LICENSE` — Licença do projeto.
- `README.md` — Este arquivo gerado contendo instruções e descrições.

> Observação: Se já existir um `README.md` no repositório, este arquivo foi gerado como `README.md` para evitar sobrescrita automática. Você pode renomeá-lo para `README.md` caso queira substituí-lo.

## Pré-requisitos

Nenhum ambiente especial é necessário para executar as páginas — um navegador web é suficiente. Para evitar problemas de CORS ao carregar JSON via `fetch`, recomenda-se servir os arquivos por um servidor HTTP local.

Exemplo rápido (Python 3):

```
python -m http.server 8000
```

Depois abra `http://localhost:8000/index.html` no navegador.

## Como usar

- Abrir `index.html` no navegador para acessar a aplicação.
- Use `search.html` para procurar por termos ou códigos.
- Abra `cutter_table.html` ou `pha_table.html` para visualizar as tabelas completas.

Se estiver usando o servidor local (recomendado), acesse as páginas via `http://localhost:8000/`.

## Formato dos arquivos JSON

As duas famílias de arquivos (`tabela_* .json` e `tabela_*_leitura.json`) seguem este propósito:

- `tabela_<nome>.json` — formato pensado para consumo pela interface (pode conter objetos com chaves como `codigo`, `descricao`, `categoria`, etc.).
- `tabela_<nome>_leitura.json` — versão destinada a leitura humana (strings prontas para exibição) ou com campos já formatados.

Exemplo simplificado (estrutura típica):

```
[
  {
    "codigo": "123.45",
    "titulo": "Assunto Exemplo",
    "descricao": "Descrição resumida deste código"
  },
  ...
]
```

A interface espera arrays de objetos; se você alterar o formato JSON, atualize também os scripts nas páginas HTML que fazem o `fetch` e processam os dados.

## Personalização

- Para adicionar/editar entradas, atualize os arquivos `tabela_*.json` correspondentes.
- Para mudar colunas ou aparência, edite os arquivos HTML e qualquer script JS embutido.

## Desenvolvimento

- Servir localmente com `python -m http.server` ou qualquer servidor estático.
- Teste mudanças abrindo as páginas no navegador apontando para o servidor local.

## Contribuição

Contribuições são bem-vindas:

- Abra uma issue descrevendo a melhoria ou correção.
- Envie um pull request com mudanças claras e testadas.

## Licença

Veja o arquivo `LICENSE` neste repositório para detalhes sobre a licença.

## Contato

Se precisar de ajuda ou quiser discutir melhorias, abra uma issue no repositório ou envie um PR.

---

Pequena nota: este README foi gerado automaticamente com base na estrutura presente nos arquivos do repositório. Ajuste exemplos e instruções conforme a necessidade do seu fluxo de trabalho.
# bibliocodes-cutter-pha
[Site](https://gpsnts.github.io/bibliocodes-cutter-pha/)
