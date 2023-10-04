# PlUG IN GERAÇÃO DE APRESENTAÇÃO
## 1. CONTEXTUALIZAÇÃO

A criação deste plugin exclusivo, compatível com o QGIS versão 3.28 e versões posteriores, surgiu como uma resposta direta à demanda por otimização na rotina de geração de apresentações de mapas de fertilidade no Departamento de Geoprocessamento da Terram Soluções Agronômicas.

O desafio central enfrentado nesse contexto diz respeito à manipulação de arquivos no formato *DTU, que contêm informações detalhadas sobre os atributos de fertilidade interpolados em uma determinada região geográfica.

Para compreender plenamente a relevância desse plugin, é necessário aprofundar-se no contexto. A fertilidade do solo é uma variável de suma importância para a agricultura, uma vez que tem um impacto direto na produtividade das culturas. Portanto, a capacidade de criar mapas de fertilidade precisos e apresentá-los de maneira eficaz é de extrema importância tanto para agricultores quanto para agrônomos e pesquisadores agrícolas.

Entretanto, a integração eficaz do formato *DTU em apresentações de PowerPoint tem se mostrado uma lacuna significativa, muitas vezes exigindo um processo repetitivo de colagem de mapas nas apresentações. O propósito fundamental deste plugin é preencher essa lacuna, proporcionando uma solução que simplifica consideravelmente a incorporação de informações de fertilidade interpoladas em apresentações.

Essa inovação não apenas simplifica o processo de criação de mapas de fertilidade, mas também amplia as possibilidades de comunicação visual no âmbito da agricultura. A seguir, exploraremos detalhadamente como esse plugin  opera e como ele pode ser utilizado para aprimorar a forma como os usuários apresentam seus dados de fertilidade do solo de maneira eficaz.

## 2. DESAFIOS NA APLICAÇÃO do _FarmCrawler_ NA CRIAÇÃO DE MAPAS DE FERTILIDADE
### 2.1 Organização dos Nomes de Talhões e Hectares

A manipulação e identificação dos talhões e hectares em sua geometria correspondente é um processo que pode ser bastante demorado, especialmente quando lidamos com perímetros extensos. Isso não apenas torna a tarefa complexa, mas também consome uma quantidade significativa de tempo.

https://github.com/SouzaVI/GERAR-APRESENTACAO/assets/98165012/2fb7e2df-3d51-4f21-9f82-9a92b769dbb4

### 2.2 Copiar e Colar Mapas no PowerPoint

A repetição do processo de copiar e colar cada mapa de fertilidade apresenta diversas desvantagens. Isso pode levar a erros de alinhamento das imagens, falta de padronização entre os mapas, potenciais enganos de digitação e, além disso, consome considerável tempo na execução das etapas de cópia, colagem, inserção de médias, organização dos mapas por atributos e profundidade.

https://github.com/SouzaVI/GERAR-APRESENTACAO/assets/98165012/b412de79-ab00-413d-9e28-e92ff253208d

## 3. USO DO PLUG IN LAYOUT (GERAR APRESENTAÇÃO) PARA OTIMIZAÇÃO DO PROCESSO DE ELABORAÇÃO DE MAPAS DE FERTILIDADE
O plugin foi criado especificamente para o QGIS 3.28 e versões posteriores. Cada aspecto da interface, funcionalidades e demais recursos foi meticulosamente projetado para efetivamente melhorar o processo de criação de mapas.

### 3.1 Pré - Requisitos
   #### 3.1.1 Caminho de pastas
No disco C:/, é necessário criar as seguintes pastas:

Disco C:

 `1. geoprocessamento`

  `1.1 estilos`

  `1.2 FERTILIDADE `

Na pasta estilos  serão armazenados arquivos QML com estilos pré-definidos para cada atributo de fertilidade.   

#### 3.1.2 Instalação das dependências e instalação do Plugin no Qgis
No ambiente OSgeo4W instale os seguintes pacotes:

`python -m pip install python-pptx`

`python -m pip install dbfread`

No qgis ir em complementos  e instale a partir de um zip a versão do plug in mais atualizada

### 3.2 Apresentação da tela
Após a instalação do plug-in, você o encontrará na barra de ferramentas, onde seu ícone é semelhante ao do PowerPoint. Se você não visualizar o ícone, pode ser necessário habilitar o plug-in. Para fazer isso, vá até a seção de complementos, selecione "Gerenciar e instalar complementos", vá para a guia "Instalados" e ative o plug-in chamado **Gerar Apresentação**.

![Imagem3](https://github.com/SouzaVI/GERAR-APRESENTACAO/assets/98165012/06feca9f-3aaf-4398-8e60-16bcf46343ad)

A tela foi projetada com o objetivo de acompanhar e facilitar o fluxo de trabalho necessário para o sucesso da produção final. Ela desempenha um papel crucial em garantir que todas as etapas essenciais sejam seguidas de forma organizada e eficiente, contribuindo assim para a obtenção do produto final com êxito.

> **1.A função descompactará o arquivo DTU na pasta FERTILIDADE, organizando os arquivos descompactados em uma subpasta com o nome do cliente, todos dentro da mesma pasta.**

> **2. Após a descompactação do DTU, o usuário deverá selecionar a pasta descompactada.**

> **3. O processo de elaboração do layout de impressão dentro do QGIS começa com a necessidade do usuário de organizar a disposição dos nomes dos talhões e hectares. Essa etapa é absolutamente crucial e requer atenção, pois servirá como base para as etapas subsequentes do processo.**

> **4. Durante esta fase, será criado um projeto individual para cada atributo de fertilidade identificado na pasta descompactada. Esses projetos serão armazenados na mesma pasta, com o propósito de simplificar qualquer modificação que possa ser necessária em um atributo específico.**

> **5. A função é responsável em exportar os layout de impressão de cada projeto em formato PNG**

> **6. 7. e 8 Lista de verificação, na qual em cada item você deve escolher apenas uma das opções disponíveis.**

> **9. A função tem a responsabilidade de extrair as imagens anexadas ao modelo de apresentação especificado, incorporando também as médias dos atributos em cada página do slide.**

![Imagem5](https://github.com/SouzaVI/GERAR-APRESENTACAO/assets/98165012/360751a4-ab3d-404e-b987-09a4bb1e596b)






