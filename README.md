<!--
*** Thanks for checking out this README Template. If you have a suggestion that would
*** make this better, please fork the repo and create a pull request or simply open
*** an issue with the tag "enhancement".
*** Thanks again! Now go create something AMAZING! :D
-->





<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/othneildrew/Best-README-Template">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Vale Incid</h3>

  <p align="center">
    App para controle de incidentes de segurança do trabalho da Vale. O objetivo é registrar, acompanhar e plotar resultados utilizando de um workflow definido.
    <br />
    <a href="https://github.com/othneildrew/Best-README-Template"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/othneildrew/Best-README-Template">View Demo</a>
    ·
    <a href="https://github.com/othneildrew/Best-README-Template/issues">Report Bug</a>
    ·
    <a href="https://github.com/othneildrew/Best-README-Template/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
## Table of Contents

* [About the Project](#about-the-project)
  * [Built With](#built-with)
* [Getting Started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
* [Usage](#usage)
* [Roadmap](#roadmap)
* [Contributing](#contributing)
* [License](#license)
* [Contact](#contact)
* [Acknowledgements](#acknowledgements)



<!-- ABOUT THE PROJECT -->
## About The Project

O porque:
Hoje na Vale o registro e controle dos incidentes é complexo e cheio de ruídos. Para que um registro seja feito, o mesmo passa por pelo
menos 3 personagens diferentes, em momentos diferentes. Por isso, um número excessivo de informação é gerada de forma repetida, é
dificil acompanhar os gargalos de atraso e a quantidade de erros é de registro é consideravel. 

Por isso, resumidamente nosso app promete:
* Definir perfis de usuários, alocando as responsabilidades de cada para que possam ser cobrados e também guiar as telas especificas para cada especialidade de perfil.
* Criar um workflow de farois, onde emails seriam disparados a medida que incidentes mais graves fossem registrados, ou quando prazos de registros estivessem em atraso.
* Levar informação a mão dos gestores, sobre as taxas e incidentes que ocorreram de forma imediata.


### Built With]

* [Javascript](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript)
* [React-Redux](https://react-redux.js.org/)
* [Typescript](https://www.typescriptlang.org/)
* [AWS](https://aws.amazon.com/pt/)



<!-- GETTING STARTED -->
## Getting Started

This is an example of how you may give instructions on setting up your project locally.
To get a local copy up and running follow these simple example steps.

### Prerequisites

This is an example of how to list things you need to use the software and how to install them.
* npm
```sh
npm install npm@latest -g
```

### Installation

1. Get a free API Key at [https://example.com](https://example.com)
2. Clone the repo
```sh
git clone https://github.com/your_username_/Project-Name.git
```
3. Install NPM packages
```sh
npm install
```
4. Enter your API in `config.js`
```JS
const API_KEY = 'ENTER YOUR API';
```



<!-- USAGE EXAMPLES -->
## Usage

Registro:

  Será feito por 3 tipos de usuários diferentes:
  
  1) Registrante inicial
  2) Resgrito de responsabilidade da Segurança do Trabalho
  3) Registro da Saúde

#User-1 Nosso User-1 é o homem de segurança de ponta, que irá descrever com fotos e palavras o incidente. A interface deste com o app 
acontece um única vez por incidente (a não ser que ele tenha de editar o mesmo por erro, caso User-2 ou User-3 verifique alguma
incongruência)

#User-2 Este é o analista de seg., responsável por avaliar o incidente, cobrar a responsabilidade dos outros Users e concluir o
registro.

#User-3 Este é o funcionário da saúde. Tem como objetivo identificar o tipo de lesão que gerou o incidente, Este entra em momento
intermediário e sem ele o incidente não pode ser concluído pelo User-2.

Objetivamente o app consistirá quanto a etapa de registro nas seguintes Telas:

  *Login
  *Tela de incidentes:
      Terá todos os incidentes com os seguintes status por User:
        
        #User-2: 
          Mostrará todos os incidentes, independente de quem seja. Será possível identificar: 
            - com quem está o registro
            - quais já foram inseridos no SAP e quais não
            - Alocar responsabilidade de incidentes a determinados Users.
          Também será capaz de tirar um relatório do incidente em PDF padrão Vale, com foto e informações.
        
        #User-1:
            Terá apenas a opção de registrar um novo incidente através de um botão + e editar os incidentes que estiverem
          alocados em sua chave de usuário.
         
        #User-3:
            Irá encontrar apenas incidentes em seu nome e incidentens aguardando resposta da saúde sem responsável.
            
    *Tela de registro:
        É o form de registro dos dados. Teremos telas diferentes para cada usuário. Esta tela é aberta ao clicar em um incidente
      ou ao criar um novo.
      
 Outras funcionalidades:
    *Workflow de registros:
        Emails devem ser disparados para diferentes pessoas por diferentes motivos.
            - Ao ser lançado um incidente de alto risco
            - quando incidentes estiverem demorando para serem finalizados seu registro.
     
     *Gerar PDF Padrão Vale do incidente selecionado.
     
     *Plotar gráficos para gestores:
          Outro perfil de usuário é o do Gestor. Este tem interesse em apenas conferir dados e gráficos a mão e on time.
          Uma nova tela seria criada apenas para apresentarmos gráficos e dados do banco de dados que criamos.
       

<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/othneildrew/Best-README-Template/issues) for a list of proposed features (and known issues).



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.



<!-- CONTACT -->
## Contact

Your Name - [@your_twitter](https://twitter.com/your_username) - email@example.com

Project Link: [https://github.com/your_username/repo_name](https://github.com/your_username/repo_name)



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
* [Img Shields](https://shields.io)
* [Choose an Open Source License](https://choosealicense.com)
* [GitHub Pages](https://pages.github.com)
* [Animate.css](https://daneden.github.io/animate.css)
* [Loaders.css](https://connoratherton.com/loaders)
* [Slick Carousel](https://kenwheeler.github.io/slick)
* [Smooth Scroll](https://github.com/cferdinandi/smooth-scroll)
* [Sticky Kit](http://leafo.net/sticky-kit)
* [JVectorMap](http://jvectormap.com)
* [Font Awesome](https://fontawesome.com)





<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=flat-square
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=flat-square
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=flat-square
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=flat-square
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=flat-square
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
