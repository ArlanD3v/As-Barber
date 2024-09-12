
## Getting Started

Primeiro, inicie o ambiente de desenvolvimento:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Abra [http://localhost:3000](http://localhost:3000) com seu navegador para visualizar a pagina.

-You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

-This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Comandos e ferramentas utilizadas no Setup do projeto:
    (Next JS)
1-> npx create-next-app@latest
        Coloque o nome do seu projeto: my-app
        Marque sim para usar o TypeScript: No / Yes
        Marque sim para usar o ESLint? No / Yes
        Marque sim para usar o Tailwind CSS? No / Yes
        Marque não para criar `src/` directory? No / Yes
        Marque sim para usar App Router? (recommended) No / Yes
        Marque sim para usar `next dev`?  No / Yes
        Marque não em import alias (`@/*` by default)? No / Yes
        >> What import alias would you like configured? @/* No

    (Prisma)
2-> npm install prisma --save-dev  (Instala o Prisma)
    npx prisma init --datasource-provider postgresql  (Passa o postgresql para informar ao Prisma que sera usado o Postgresql como Banco)
        -Ele vai criar um arquivo .env onde tem o Database_URL, ai é so acessar o Neondb para pegar a URL
        - Para migrar o banco criado em ./prisma/schema.prisma execute:
    npx prisma migrate dev --name init_db
    O comando acima vai criar uma migrations em modo de desenvolvimento
    -Dentro de package.json insira : abaixo de scripts >  
                    "prisma": {
                    "seed": "ts-node prisma/seed.ts" }
    -Tem um arquivo dentro de ./prisma chamado seed.ts que preenche o banco de dados, para conseguir rodar ele é necessario instalar o ts-node com comando:
    npm install -D ts-node  (Depois execute :)
    npx prisma db seed      (Esse comando executa o Script dentro de Seed.ts)

    (Prettier para Tailwindcss)
3-> npm install -D prettier prettier-plugin-tailwindcss
      Crie na pasta raiz um arquivo chamado .prettierrc.json e insira :
                                        {
                                    "plugins": [
                                        "prettier-plugin-tailwindcss"
                                    ],
                                    "tabWidth": 2,
                                    "semi": false
                                    }
    
    (Shadcn.ui)
4-> npx shadcn-ui@latest init
Ele cria as pastas ./lib e ./components  (caso ele não crie a componets, ele cria quando você instalar algum componente disponibilizado no site do shadcn)
em components.json você configura o caminho

