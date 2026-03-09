# 🚀 CI Example com GitHub Actions

Este repositório contém um exemplo simples de **Integração Contínua (CI)** utilizando o **GitHub Actions**.

O workflow executa automaticamente sempre que ocorre um **push** no repositório e imprime duas mensagens no log da execução.

---

# 📌 Objetivo

Demonstrar de forma simples:

- Como criar um workflow no GitHub Actions
- Como executar um pipeline automaticamente
- Como rodar comandos dentro de um job

---

# ⚙️ Workflow

O workflow está definido no arquivo:

```
.github/workflows/ci.yml
```

Conteúdo do workflow:

```yaml
name: CI Example

on: [push]

jobs:
  test:
    runs-on: ubuntu-latest

    steps:
    - name: Mensagem 1
      run: echo "Iniciando pipeline"

    - name: Mensagem 2
      run: echo "Pipeline finalizado"
```

---

# 🧠 Explicação do Workflow

## 1️⃣ Nome do Workflow

```yaml
name: CI Example
```

Define o nome do pipeline que aparecerá na aba **Actions** do repositório.

---

## 2️⃣ Evento que dispara o pipeline

```yaml
on: [push]
```

Significa que o workflow será executado **sempre que um push for realizado no repositório**.

---

## 3️⃣ Jobs

```yaml
jobs:
  test:
```

Um **job** representa um conjunto de tarefas executadas em uma máquina virtual.

Neste exemplo existe apenas um job chamado **test**.

---

## 4️⃣ Ambiente de execução

```yaml
runs-on: ubuntu-latest
```

Define que o job será executado em uma máquina virtual **Ubuntu** fornecida pelo GitHub.

---

## 5️⃣ Steps

Os **steps** são os comandos executados dentro do job.

### Step 1

```yaml
- name: Mensagem 1
  run: echo "Iniciando pipeline"
```

Mostra no log:

```
Iniciando pipeline
```

---

### Step 2

```yaml
- name: Mensagem 2
  run: echo "Pipeline finalizado"
```

Mostra no log:

```
Pipeline finalizado
```

---

# ▶️ Fluxo da Execução

Sempre que um **push** for realizado:

1. O GitHub detecta o evento
2. O workflow é iniciado
3. O job `test` é executado
4. Os dois comandos `echo` são executados
5. As mensagens aparecem no log da execução

---

# 📊 Exemplo de saída no log

```
Iniciando pipeline
Pipeline finalizado
```

---

# 🛠 Tecnologias utilizadas

- GitHub
- GitHub Actions
- YAML
- Ubuntu Runner

---

# 📚 Documentação

Documentação oficial:

https://docs.github.com/actions

---

# 👨‍💻 Autor

Projeto criado para fins de estudo de **CI/CD com GitHub Actions**.
