# Alura Album - Copa do Mundo Tech

O **Alura Album** é um tributo interativo em forma de álbum de figurinhas digital que celebra a história e a evolução da tecnologia e do desenvolvimento de software. O projeto traz cromos colecionáveis de grandes mentes nacionais e internacionais organizados por categorias como Inteligência Artificial, Python, Banco de Dados, Sistemas Operacionais e Celebridades Tech do Brasil.

---

## 🎯 Objetivo

O objetivo principal do projeto é apresentar de forma dinâmica e interativa os pioneiros e as mentes brilhantes que moldam o ecossistema da tecnologia, criando uma experiência lúdica e imersiva de "colecionar" figurinhas virtuais carregadas a partir de uma API.

---

## 🛠️ Arquivos e Funcionalidades

O projeto é construído sobre a tríade fundamental da web (`HTML`, `CSS` e `JavaScript`) e utiliza uma biblioteca externa para renderização de páginas no estilo livro físico.

### 1. [index.html](file:///c:/Users/tatit/Projetos/arquitetura_web_ia/i-arq-ia-alura-album-main/index.html)
* **Função**: Estrutura e esqueleto da aplicação.
* **Funcionalidades principais**:
  * Define as páginas física e virtualmente do álbum (capa, páginas internas temáticas e contracapa).
  * Cria os compartimentos/slots numerados de `#01` a `#30` que receberão as figurinhas.
  * Insere os elementos de controle de som, botões de navegação lateral (anterior e próximo) e a importação dos scripts e folhas de estilo.
  * Importa a biblioteca **PageFlip.js** via CDN para possibilitar a animação realista de folhear.

### 2. [style.css](file:///c:/Users/tatit/Projetos/arquitetura_web_ia/i-arq-ia-alura-album-main/style.css)
* **Função**: Identidade visual, estilização e animações do álbum.
* **Funcionalidades principais**:
  * Estabelece um tema escuro e espacial moderno usando gradientes radiais, sombras marcantes e realces em tons neon.
  * Inclui fontes personalizadas do Google Fonts (`Inter` e `Outfit`).
  * Adiciona efeitos especiais complexos, como a animação de *glitch* na tipografia da capa e a esfera tecnológica 3D pulsante.
  * Gerencia os estados de clique e arraste das páginas para indicar visualmente quando uma página está sendo folheada.
  * Implementa a estilização das figurinhas coladas e a animação de "colagem" suave (*fade-in* com escala).

### 3. [app.js](file:///c:/Users/tatit/Projetos/arquitetura_web_ia/i-arq-ia-alura-album-main/app.js)
* **Função**: Lógica de comportamento, sons e integração com backend.
* **Funcionalidades principais**:
  * **Integração com API**: Conecta-se à API local (por padrão em `http://localhost:8000`) para buscar as figurinhas e preencher os slots no álbum de forma automática.
  * **Configuração do PageFlip**: Inicializa a biblioteca de virada de páginas definindo dimensões, sombras, tempos de transição e desativando eventos de clique simples indesejados.
  * **Movimentos Personalizados**: Detecta toques, cliques e arrastes para criar transições realistas de dobra de página (suporta mouse, teclado e gestos mobile).
  * **Efeitos Sonoros**: Sintetiza em tempo real um som realista de papel virando usando a *Web Audio API* (eliminando a necessidade de arquivos de áudio externos).
  * **Controles Interativos**: Habilita o botão para mutar/desmutar o áudio e controla as setas laterais para que apareçam apenas quando fizer sentido (por exemplo, ocultando a seta esquerda quando estiver na capa).

---

## 🚀 Como Executar o Projeto

1. **Backend (API)**:
   Certifique-se de inicializar a API para que as figurinhas sejam carregadas e exibidas no álbum:
   ```bash
   cd backend/dia-3
   uvicorn main:app --reload
   ```

2. **Frontend**:
   Abra o arquivo [index.html](file:///c:/Users/tatit/Projetos/arquitetura_web_ia/i-arq-ia-alura-album-main/index.html) em seu navegador de preferência ou utilize um servidor local de desenvolvimento (como o Live Server do VS Code).
