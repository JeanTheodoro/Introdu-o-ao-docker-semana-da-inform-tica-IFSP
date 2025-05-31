🐍 # Introdução a Linguagem  Python

📚 ## Tipos de Dados e Variáveis

  *  Tipos básic
  *  Variáveis e entrada de dados
  *  operadores Aritméticos
  *  operadores Comparação
  *  operadores Lógicos

📚 ## Controle de Fluxo

  *  Condicionais
  *  Laços de repetição
  *  
📚 Strings
  *  Strings


# 🐳 Minicurso Docker – Comandos Essenciais

Aprenda os principais comandos para trabalhar com containers Docker no seu dia a dia.

---

## 📦 1. Executar um Container Docker

*Inicia um container a partir de uma imagem, executando seu processo principal.*

```bash
docker run <imagem>
```

Exemplo:

```bash
docker run nginx
```

---

## 🔧 2. Comandos de Interação com o Docker

*Utilizados para monitorar e gerenciar containers e imagens em execução ou armazenados localmente.*

```bash
docker ps                  # Lista containers em execução
docker ps -a              # Lista todos os containers (inclusive os parados)
docker stop <id>          # Para um container em execução
docker rm <id>            # Remove um container parado
docker images             # Lista todas as imagens locais
```

---

## 📁 3. Mapeamento de Diretório (Volume ou Bind Mount)

*Permite que arquivos da máquina sejam acessados ou salvos dentro do container.*

### 🔹 Volume (gerenciado pelo Docker)

```bash
docker run -v nome_volume:/app nginx
```

### 🔸 Bind Mount (diretório local)

```bash
docker run -v $(pwd)/meus_arquivos:/app nginx
```

---

## 🌐 4. Mapeamento de Porta

*Torna o serviço dentro do container acessível a partir da máquina host.*

```bash
docker run -p <porta_host>:<porta_container> <imagem>
```

Exemplo:

```bash
docker run -p 8080:80 nginx
```

---

## 🧩 5. Execução do Container no Modo Daemon

*Roda o container em segundo plano (modo detached), liberando o terminal.*

```bash
docker run -d <imagem>
```

Exemplo com NGINX:

```bash
docker run -d -p 8080:80 nginx
```

---

## 🧹 6. Comandos de Limpeza

*Remove recursos não utilizados como containers, imagens e volumes para liberar espaço.*

```bash
docker container prune     # Remove containers parados
docker image prune         # Remove imagens não utilizadas
docker volume prune        # Remove volumes não utilizados
docker system prune        # Remove tudo que não está em uso
```
