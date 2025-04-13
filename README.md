# Desafio – AEVO by Iasmin Marques

- Explorar a Documentação da API (https://pokeapi.co/docs/v2), para detalhes de
  utilização;
- Elaborar uma página para consultar e exibir as informações (lista de pokemons) da
  requisição da API na página;
- Adicionar um input na página para permitir buscas;
- Selecionar um dos pokemons listados para ver informações detalhadas (Informações
  detalhadas vem de outra requisicão na API);
- Realizar a soma de todos status (Atributo base_stats que fica dentro de stats) do
  pokemon selecionado e exibir esse valor;
- Selecionar dois pokemons e exibir qual dos dois tem a soma de status(Atributo
  base_stats que fica dentro de stats) maior;
- Documentação

## Tecnologias Utilizadas <br/>

- Angular: Framework JavaScript utilizado para a construção da aplicação.
- TypeScript: Linguagem utilizada para o desenvolvimento da lógica da aplicação.
- PokeAPI: API pública utilizada para buscar informações sobre os Pokémons.
- CSS: Estilização da interface. <br/>

## Teste - Dominio

Criei um subdomínio dentro do site de hospedagens Hostgator para testes, segue o link: </br>
http://aevo.iasminmarques.com.br

- Comparador de Status </br>
  https://aevo.iasminmarques.com.br/comparar

## Como Executar o Projeto Localmente <br/>

1. Clonar o repositório:
```
git clone https://github.com/iasminimp/poke-aevo.git
 ```
2. Instalar as dependencias:
```
npm install
```
3. Rodar o projeto:
```
ng serve
```
4. Acesse: `http://localhost:4200`

## Componentes <br/>

### ListaPokemonComponent

- Busca dinâmica por nome
- Exibe nome e imagem dos Pokémons
- Navega para a tela de detalhes <br/>

### DetalhesPokemonComponent <br/>

- Exibe altura, peso, tipos e todos os stats
- Mostra a soma total de stats
- Botão para voltar à home (nav-bar e “X”)

### ComparadorComponent <br/>

- Busca e seleciona dois Pokémons
- Exibe seus status totais e imagem
- Indica o vencedor com destaque visual
- Exibe mensagem de erro caso não selecione os dois <br/>

## API

Link da API: https://pokeapi.co/ </br>
Documentação da API: https://pokeapi.co/docs/v2

### Fase de Testes

Exemplo de requisições feitas e rotas

- Uma chamada da API para trazer 151 pokemons

```
https://pokeapi.co/api/v2/pokemon/?limit=151
```

- Uma chamada da API para trazer mais informações do pokemon 4 - Charmander

```
https://pokeapi.co/api/v2/pokemon/4/
```

- Listagem de todos os Pokémon (limit=1000 define o número máximo de resultados
  retornados)

```
https://pokeapi.co/api/v2/pokemon?limit=1000
```

- Detalhes de um Pokémon específico (Exemplo: pikachu e ditto)

```
https://pokeapi.co/api/v2/pokemon/{nome-do-pokemon}
```

## Funções para se adicionar futuramente

- Infinity scroll (adicionar paginação): atualmente a pesquisa está limitada com um
  numero de Pokémon
- Melhorar o designer/ padronizar: questões de UX/ UI da aplicação;
- Loading Spinner/ carregando: estiver buscando Pokémons, exibir um loading para dar
  uma maior fluidez;
- Em detalhes do pokemon: gráficos de radar ou barra para as estatísticas, a exibição de
  evoluções do Pokémon;
