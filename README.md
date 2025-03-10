# N1-eletiva

## 1. Descrição da Base de Dados

### 1.1 Descrição Geral do Dataset

Foi utilizado o conjunto de dados MovieLens Small, que contém informações sobre filmes, usuários, avaliações e tags. O dataset inclui quatro arquivos principais:

- **movies.csv**: Contém informações sobre filmes, incluindo identificadores e gêneros.
- **ratings.csv**: Armazena as avaliações feitas pelos usuários para diferentes filmes.
- **tags.csv**: Inclui tags atribuídas pelos usuários aos filmes.
- **links.csv**: Relaciona os filmes do MovieLens com identificadores do IMDb e TMDb.

### 1.2 Estrutura dos Arquivos

Cada linha dos arquivos representa:

- **movies.csv**: Um filme, com colunas: `movieId`, `title`, `genres`.
- **ratings.csv**: Uma avaliação de um usuário, com colunas: `userId`, `movieId`, `rating`, `timestamp`.
- **tags.csv**: Uma tag atribuída a um filme, com colunas: `userId`, `movieId`, `tag`, `timestamp`.
- **links.csv**: Identificadores externos dos filmes, com colunas: `movieId`, `imdbId`, `tmdbId`.

### 1.3 Atributos e Tipos

Os arquivos possuem os seguintes atributos e tipos de dados:

- **movies.csv**: `movieId` (int), `title` (string), `genres` (string)
- **ratings.csv**: `userId` (int), `movieId` (int), `rating` (float), `timestamp` (int)
- **tags.csv**: `userId` (int), `movieId` (int), `tag` (string), `timestamp` (int)
- **links.csv**: `movieId` (int), `imdbId` (int), `tmdbId` (float, com valores nulos)

---

## 2. Preparação da Base de Dados

### 2.1 Problemas Identificados

- O campo `tmdbId` em **links.csv** contém valores nulos e deve ser ajustado.
- O campo `genres` em **movies.csv** está formatado como uma string com gêneros separados por `|`, dificultando análises futuras.
- O campo `timestamp` nos arquivos **ratings.csv** e **tags.csv** está no formato UNIX, necessitando conversão para uma data legível.
- Possíveis valores nulos em algumas colunas dos arquivos.

### 2.2 Correções Aplicadas

- Conversão de `tmdbId` para inteiro e substituição de valores nulos por `0`.
- Transformação da coluna `genres` para listas de gêneros separados.
- Conversão de `timestamp` para formato de data legível.
- Substituição de valores nulos nos datasets por "N/A".



