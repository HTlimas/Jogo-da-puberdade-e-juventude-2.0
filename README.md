# Crescendo com Confiança

Jogo educativo 2D sobre **puberdade, saúde, hábitos saudáveis e Bem Viver**, ambientado em **Camaçari, Bahia**.

Desenvolvido com **HTML5 + CSS3 + JavaScript + Phaser 3**.

## Personagens

- **Lucas Tavares** (14 anos) – Campanha principal masculina
- **Lara** (14 anos) – Campanha principal feminina (inclui conteúdo sobre menstruação)

## Como executar

### Opção 1 – Live Server (VS Code)
1. Abra a pasta do projeto no Visual Studio Code
2. Instale a extensão **Live Server**
3. Clique com o botão direito em `index.html` → **Open with Live Server**

### Opção 2 – Qualquer servidor local
```bash
# Com Python
python -m http.server 8000

# Com Node (npx)
npx serve .
```
Acesse `http://localhost:8000`

### Opção 3 – Vite (recomendado para desenvolvimento)
```bash
npm create vite@latest . -- --template vanilla
# (ou apenas abra com Live Server por enquanto)
```

## Controles

| Tecla / Mouse | Ação |
|---------------|------|
| Setas / WASD | Mover |
| E ou Clique | Interagir com NPCs / Hotspots de rotina |
| R | Abrir menu de Rotina Diária |
| ESC | Menu de Pausa |
| I | Inventário |
| M | Mapa |
| Espaço / Enter / Clique | Avançar diálogo |

## Sistema de Clima e Rotina

### Clima
- Ensolarado, Nublado, Chuvoso, Tempestade, Neblina
- Muda automaticamente; overlay visual + partículas de chuva
- Efeitos leves em energia, felicidade e saúde

### Ciclo Dia/Noite
- Tempo avança continuamente (minutos e horas)
- Períodos: Amanhecer → Manhã → Tarde → Entardecer → Noite
- Overlay de cor muda conforme o período
- Novo dia reseta flags diárias de rotina

### Rotina Diária (tecla R ou hotspots no mapa)
- Dormir (casa) – recupera energia e saúde
- Higiene – aumenta higiene e autoestima
- Comer equilibrado / Comer doces – impactos diferentes
- Exercício (quadra) – melhora saúde e felicidade
- Estudar – aumenta conhecimento
- Conversar com a família – felicidade e respeito
- Stats degradam com o tempo se a rotina for negligenciada

## Estrutura do Projeto

```
jogo-puberdade/
├── index.html
├── README.md
├── src/
│   ├── main.js
│   ├── styles.css
│   ├── systems/
│   │   ├── TimeWeatherSystem.js
│   │   └── RoutineSystem.js
│   ├── scenes/
│   │   ├── BootScene.js
│   │   ├── PreloadScene.js
│   │   ├── TitleScene.js
│   │   ├── CharacterSelectScene.js
│   │   ├── RoutineMenuScene.js
│   │   ├── WorldScene.js
│   │   ├── DialogueScene.js
│   │   ├── UIScene.js
│   │   ├── PauseScene.js
│   │   ├── InventoryScene.js
│   │   ├── MapScene.js
│   │   ├── ScienceFairScene.js
│   │   └── EndingScene.js
│   ├── entities/
│   ├── systems/
│   ├── ui/
│   ├── data/
│   └── assets/
```

## Capítulos (Campanha)

1. Um Novo Começo
2. As Primeiras Mudanças / O Início da Puberdade
3. Conhecendo Meu Corpo / Espelho da Verdade
4. Higiene é Cuidado
5. Menstruação sem Medo (Lara) / Dormir ou Virar a Noite? (Lucas)
6. Alimentação Faz Diferença
7. Corpo em Movimento
8. Emoções e Hormônios
9. Pressão dos Colegas
10. Verdade ou Mito?
11. Cada Pessoa Tem Seu Tempo
12. Autoestima e Respeito / Hábitos Saudáveis
13. Projeto da Feira / Compartilhando Conhecimento
14. Trabalho em Equipe / O Grande Desafio
15. Uma Nova Lara / Um Novo Lucas – Certificado

## Objetivos Educacionais

- Puberdade e hormônios
- Higiene e autocuidado
- Alimentação saudável
- Sono e rotina
- Emoções
- Respeito às diferenças
- Bem Viver e cidadania
- Busca por informações confiáveis
- Saúde preventiva (UBS)

## Status

**Versão inicial funcional** – Menu, seleção de personagem, mundo explorável, diálogos, inventário, mapa, pausa, salvamento local e finalização básica implementados.

Próximos módulos: sistema de missões completo, lojas, clima, economia avançada, mais mapas internos (casa, escola, UBS), animações de personagens, quests secundárias e conteúdo completo dos 15 capítulos.

---

Desenvolvido para fins educacionais.  
Inspirado em RPGs clássicos (estilo Pokémon), com identidade visual própria.
