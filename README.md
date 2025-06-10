# sistema-biblioteca-digital
Sistema em Python para gerenciamento de documentos digitais (PDF, ePUB etc.) de uma biblioteca universitária.

## Funcionalidades
- Listar documentos digitais disponíveis
- Adicionar documentos (via upload no Colab)
- Renomear e remover documentos
- Organizar documentos por tipo e ano de publicação

## Como usar no Google Colab
1. Crie um arquivo chamado 'documentos' no ficheiro do google colab ou execute o código 
`os.makedirs('documentos', exist_ok=True)`

2. Execute a célula com a função `adicionar_documento_upload()` para enviar arquivos.

3. Depois use outras funções:

```python
listar_documentos()
renomear_documento('arquivo.pdf', 'novo_nome.pdf')
remover_documento('novo_nome.pdf')
organizar_documentos()
```

## Estrutura do Projeto
Os arquivos são organizados automaticamente conforme sua extensão e ano:

*caso o arquivo não possua ano, ele se encontrará na pasta desconhecido*

```
documentos/
├── pdf/
│   └── 2023/
└── epub/
    └── desconhecido/
```

##  Requisitos
- Python 3.x
- Google Colab (com `google.colab.files`)
