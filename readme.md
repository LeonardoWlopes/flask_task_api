# Flask Task API

Este é um aplicativo Flask para gerenciar tarefas.

## Endpoints disponíveis

- `POST /tasks`: Cria uma nova tarefa.
- `GET /tasks`: Retorna a lista de tarefas existentes.
- `GET /tasks/<int:task_id>`: Retorna os detalhes de uma tarefa específica.
- `PUT /tasks/<int:task_id>`: Atualiza os detalhes de uma tarefa específica.
- `PATCH /tasks/<int:task_id>`: Alterna o status de conclusão de uma tarefa específica.
- `DELETE /tasks/<int:task_id>`: Exclui uma tarefa específica.

## Uso

Certifique-se de ter o Flask instalado antes de executar este aplicativo.

## API

### Criação de uma nova tarefa

- **URL**: `/tasks`
- **Método**: `POST`
- **Parâmetros**:
    - `title` (str): O título da tarefa.
    - `description` (str, opcional): A descrição da tarefa.
- **Retorno**:
    - **Código de status**: 201 (Tarefa criada com sucesso)
    - **Corpo**: JSON contendo os detalhes da nova tarefa criada.

### Listagem de tarefas existentes

- **URL**: `/tasks`
- **Método**: `GET`
- **Retorno**:
    - **Código de status**: 200 (Requisição bem-sucedida)
    - **Corpo**: JSON contendo a lista de tarefas existentes e o total de tarefas.

### Detalhes de uma tarefa específica

- **URL**: `/tasks/<int:task_id>`
- **Método**: `GET`
- **Parâmetros**:
    - `task_id` (int): O ID da tarefa.
- **Retorno**:
    - **Código de status**: 200 (Requisição bem-sucedida) ou 404 (Tarefa não encontrada)
    - **Corpo**: JSON contendo os detalhes da tarefa.

### Atualização de uma tarefa específica

- **URL**: `/tasks/<int:task_id>`
- **Método**: `PUT`
- **Parâmetros**:
    - `task_id` (int): O ID da tarefa.
    - `title` (str): O novo título da tarefa.
    - `description` (str, opcional): A nova descrição da tarefa.
    - `completed` (bool, opcional): O novo status de conclusão da tarefa.
- **Retorno**:
    - **Código de status**: 200 (Requisição bem-sucedida) ou 404 (Tarefa não encontrada)
    - **Corpo**: JSON contendo os detalhes da tarefa atualizada.

### Alteração do status de conclusão de uma tarefa específica

- **URL**: `/tasks/<int:task_id>`
- **Método**: `PATCH`
- **Parâmetros**:
    - `task_id` (int): O ID da tarefa.
- **Retorno**:
    - **Código de status**: 200 (Requisição bem-sucedida) ou 404 (Tarefa não encontrada)
    - **Corpo**: JSON contendo os detalhes da tarefa atualizada.

### Exclusão de uma tarefa específica

- **URL**: `/tasks/<int:task_id>`
- **Método**: `DELETE`
- **Parâmetros**:
    - `task_id` (int): O ID da tarefa.
- **Retorno**:
    - **Código de status**: 200 (Requisição bem-sucedida) ou 404 (Tarefa não encontrada)
    - **Corpo**: JSON contendo uma mensagem informando que a tarefa foi excluída com sucesso.

## Execução

Para executar o aplicativo, execute o seguinte comando no terminal:
```bash
python app.py
```
