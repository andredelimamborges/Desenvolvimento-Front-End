# Desenvolvimento-Front-End

# Gato Preto do Destino

**Bem-vindo ao Gato Preto do Destino!** Este é um site interativo que explora pontos turísticos da América Latina e permite que os usuários ouçam sons das capitais do mundo enquanto aguardam o destino aleatório que a página oferece. Inspirado no conceito de "azar" do "Gato Preto", este site proporciona uma experiência única, onde a sorte de onde você vai parar fica nas mãos do acaso a cada atualização de página.

---

## Funcionalidades Principais

1. **Previsão do Tempo para Destinos Turísticos da América Latina**:
   - O site exibe informações climáticas sobre uma cidade turística da América Latina, escolhida aleatoriamente toda vez que a página é carregada. 
   - O usuário também pode inserir manualmente o nome de uma cidade para obter a previsão do tempo.

2. **Sons Ambientais ao Vivo**:
   - Uma seção central com um `iframe` integrado ao site [Drive & Listen](https://driveandlisten.herokuapp.com/) permite que os usuários escutem sons ao vivo de várias cidades pelo mundo, oferecendo uma experiência imersiva de "ruídos sonoros" de várias metrópoles globais.

3. **Artigos e Notícias**:
   - Uma seção de "Artigos e Notícias" oferece conteúdos relacionados aos pontos turísticos e atualizações sobre as principais capitais da América Latina.

---

## Estrutura do Projeto

- **index.html**: Estrutura básica do site, incluindo um cabeçalho com um campo de pesquisa para a cidade, uma seção `iframe` com sons ao vivo e uma área para exibir as condições climáticas de uma cidade.
- **index.css**: Arquivo de estilos que configura o layout, cores e estilização dos elementos, centralizando o `iframe` e estilizando a interface.
- **integracao.js**: Script principal para interagir com a API de clima e exibir as condições climáticas.

---

## Detalhes do Script (`integracao.js`)

O script `integracao.js` lida com a exibição das informações de previsão do tempo para uma cidade escolhida aleatoriamente a cada carregamento da página. Abaixo está um resumo das principais funções:

1. **Configurações Iniciais**:
   - `apiKey`: Chave da API do OpenWeather para obter as informações climáticas.
   - `cities`: Array com uma lista de cidades turísticas da América Latina, como "Rio de Janeiro", "Buenos Aires" e "Cancún".

2. **Função `getRandomCity()`**:
   - Escolhe aleatoriamente uma cidade do array `cities`, retornando o nome da cidade para exibição automática ao carregar a página.

3. **Função `getWeather(city)`**:
   - Recebe o nome de uma cidade e busca os dados climáticos dela na API do OpenWeather.
   - Formata a URL com o nome da cidade e a `apiKey`, configurando a temperatura em graus Celsius e descrição em português.
   - Faz uma requisição `fetch()` para a API, e se bem-sucedida, exibe os dados na `div` com `id="weather"`. Caso contrário, exibe uma mensagem de erro.

4. **Carregamento de Cidade Aleatória**:
   - Quando a página é carregada, o evento `window.load` chama `getRandomCity()` e, em seguida, `getWeather()` para exibir a previsão do tempo de uma cidade aleatória.
   

---

## Tecnologias Utilizadas

- **HTML, CSS, JavaScript**: Estrutura e estilização do site.
- **OpenWeather API**: Para fornecer informações climáticas das cidades.
- **Drive & Listen**: Um `iframe` do site para proporcionar sons ao vivo de várias cidades.

---

