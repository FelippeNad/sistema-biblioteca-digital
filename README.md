# sistema-biblioteca-digital
Sistema em Python para gerenciamento de documentos digitais (PDF, ePUB etc.) de uma biblioteca universitária.

## Funcionalidades
- Listar documentos digitais disponíveis
- Adicionar documentos (via upload no Colab)
- Renomear e remover documentos
- Organizar documentos por tipo e ano de publicação

## Como usar no Google Colab
1. Crie um arquivo chamado 'documentos' no ficheiro do google colab ou execute o código
   
```python
os.makedirs('documentos', exist_ok=True)
```

2. Execute a célula com a função `adicionar_documento_upload()` para enviar arquivos.

3. Depois use outras funções:

```python
listar_documentos()
renomear_documento('arquivo.pdf', 'novo_nome.pdf')
remover_documento('novo_nome.pdf')
organizar_documentos()
```
---

##  Funcionalidades do Sistema

### ✅ 1. `adicionar_documento_upload()`
- Abre uma janela para você fazer upload de arquivos diretamente do seu computador.
- Todos os arquivos enviados são automaticamente movidos para a pasta `documentos/`.

### ✅ 2. `listar_documentos()`
- Exibe todos os arquivos que estão atualmente na pasta `documentos/`.
- Ajuda o usuário a visualizar os documentos antes de organizar, renomear ou remover.

### ✅ 3. `organizar_documentos()`
- Organiza os documentos que estão na pasta `documentos/` de forma automática.
- Primeiro separa por **tipo de arquivo** (ex: `pdf`, `epub`) e depois por **ano** (os 4 últimos números do nome do arquivo).
- *caso o arquivo não possua ano, ele se encontrará na pasta desconhecido*
- Exemplo de estrutura gerada:
```
documentos/
├── pdf/
│   ├── 2023/
│   └── desconhecido/
└── epub/
    └── 2022/
```

### ✅ 4. `renomear_documento(nome_antigo, nome_novo)`
- Altera o nome de um arquivo que está na pasta `documentos/`.
- Exemplo de uso:
```python
renomear_documento('livro.pdf', 'livro_tese.pdf')
```

### ✅ 5. `remover_documento(nome)`
- Exclui permanentemente um arquivo da pasta `documentos/`.
- Exemplo de uso:
```python
remover_documento('livro_tese.pdf')
```

---

##  Requisitos
- Python 3.x
- Google Colab (com `google.colab.files`)
