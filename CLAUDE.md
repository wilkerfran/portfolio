# Portfólio — Wilker França

## Objetivo
Portfólio pessoal de dev fullstack (React, TypeScript, FastAPI, PostgreSQL, GCP).
Foco em vagas, inclusive internacionais. Vibe: desenvolvedor nerd, dark, cinematográfico.
Referência de linguagem visual: landonorris.com (tipografia gigante, motion, hero líquido).
NÃO copiar a identidade do Lando (cores lima/oliva, fonte Brier, logo).

## Stack
- Vite + React + TypeScript
- Tailwind CSS v4 (@tailwindcss/vite), tokens em src/styles/index.css via @theme
- three + @react-three/fiber + @react-three/drei (hero líquido com shader GLSL)
- gsap (reveals com clip-path/transform), lenis (smooth scroll)
- Deploy: Netlify

## Estrutura
src/sections/        Hero, About, Projects, Stack, Experience, Contact
src/components/      layout/ (Header, Footer) e ui/ (botões, tags)
src/webgl/           canvas + shaders/*.glsl (importar com ?raw)
src/hooks/           useLenis etc.
src/data/            conteúdo em TS (projetos, experiência), separado do layout
public/fonts/        MonaSans.woff2 (variável, self-hosted)
Nada de projeto em arquivo único: um componente por arquivo.

## Design tokens
Cores: ink-950 #08090B (fundo), ink-900 #0D0F12, ink-800 #15181D (cards),
ink-700 #22262D, bone #ECEAE3 (texto), mute #8B9099 (secundário),
signal #3DE8FF (destaque principal, glow do monitor), ember #FFB547 (destaque raro).
Fontes: Mona Sans (display, wdth 75–125, wght 200–900) e JetBrains Mono (labels/código).
Display: uppercase, line-height 0.85–0.9, letter-spacing negativo, 80–140px no desktop.
Motion: 0.75s, cubic-bezier(0.65, 0.05, 0, 1); reveals com clip-path e transform.
Raios: botão 10px, card 56px.

## Hero
Efeito líquido em WebGL (displacement com noise reagindo ao mouse).
Foto: public/images/ — versão completa + versão recortada (PNG sem fundo),
o shader distorce o fundo e a pessoa fica nítida por cima.

## Convenções
- Componentes funcionais, nomes em inglês, textos do site em PT-BR (EN depois).
- Respeitar prefers-reduced-motion (desligar shader/animações pesadas).
- Trabalhar passo a passo: mostrar o plano antes de grandes mudanças.
