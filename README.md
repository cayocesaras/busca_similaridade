# Sistema de Recomendação por Similaridade Visual

## Visão Geral

Este projeto desenvolve um **Sistema de Recomendação de Produtos baseado em Similaridade Visual**, indo além dos métodos tradicionais que utilizam apenas dados textuais (preço, modelo, marca). Nosso objetivo é recomendar produtos que sejam visualmente semelhantes em termos de **formato, cor, textura e estilo**, proporcionando uma experiência de busca mais intuitiva para o usuário.

O sistema utiliza técnicas de **Deep Learning** para extrair características visuais de imagens de produtos, permitindo que a similaridade seja calculada com base na aparência física.

---

## Funcionalidades

* **Extração de Features Visuais:** Utiliza uma rede neural convolucional pré-treinada para gerar vetores de características (embeddings) que representam a aparência visual de cada produto.
* **Busca por Similaridade:** Compara a imagem de um produto consultado com o catálogo existente para encontrar e recomendar itens visualmente parecidos.
* **Foco em Similaridade Intra-Classe:** O modelo é treinado para distinguir e agrupar produtos que são parecidos em sua aparência, mesmo dentro da mesma categoria geral.

---

## Tecnologias Utilizadas

* **Python:** Linguagem principal de desenvolvimento.
* **TensorFlow/Keras:** Framework para construção e utilização do modelo de Deep Learning.
* **Numpy:** Para manipulação eficiente de vetores numéricos (features).
* **Scikit-learn:** Para cálculo da similaridade (similaridade de cosseno).
* **Matplotlib:** Para visualização das imagens e resultados.

---

## Classes de Produtos (Categorias)

O modelo foi treinado e testado com 4 classes específicas de produtos, focando em obter uma boa representação da variação visual dentro de cada uma:

* `[Nome da Classe 1, ex: Relógios]`
* `[Nome da Classe 2, ex: Camisetas]`
* `[Nome da Classe 3, ex: Sapatos]`
* `[Nome da Classe 4, ex: Bicicletas]`

*(Atenção: Lembre-se de substituir os nomes de exemplo pelas suas classes reais!)*

---

## Como Usar (Google Colab)

Este projeto é configurado para ser executado facilmente no **Google Colab**, aproveitando sua infraestrutura gratuita de GPU.

1.  **Clone o Repositório:** Faça o download ou clone este repositório para sua máquina local.
2.  **Organize seu Dataset:**
    * No seu Google Drive, crie uma pasta raiz para o dataset (ex: `meu_dataset_similaridade`).
    * Dentro dela, crie subpastas para cada uma das 4 classes de produtos (ex: `relogios/`, `camisetas/`).
    * Faça o upload de suas imagens para as respectivas subpastas. Recomenda-se **200-500 imagens por classe** para bons resultados.
3.  **Abra o Notebook no Colab:**
    * Vá para [Google Colab](https://colab.research.com/).
    * Clique em `File` -> `Upload notebook` ou `File` -> `Open notebook` e selecione o arquivo `.ipynb` deste projeto.
4.  **Execute as Células:**
    * Siga as instruções no notebook do Colab para montar seu Google Drive e ajustar o `dataset_path`.
    * Execute as células sequencialmente para instalar dependências, extrair as features visuais do seu dataset e realizar a busca por similaridade.
    * Para testar, faça o upload de uma `imagem de consulta` para o ambiente do Colab e ajuste o `query_product_image` no código.

---

## Estrutura do Projeto
.
├── README.md
├── seu_notebook_colab.ipynb  # (O arquivo .ipynb que contém o código do Colab)
└── (Opcional: outras pastas como data/ se não usar o Drive)

---

## Contribuição

Contribuições são bem-vindas! Se você tiver sugestões ou melhorias, sinta-se à vontade para abrir uma issue ou enviar um pull request.

---

## Licença

[MIT License](LICENSE) (Recomendado: Crie um arquivo `LICENSE` no seu repositório com os termos da licença MIT ou outra de sua preferência.)
