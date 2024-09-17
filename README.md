<h1 align="center">AS Barber</h1>

<h3 align="center"> :computer: Funcionalidades </h3>
Projeto inspirado no FSW com intuito da criação de um APP para barbearias, onde o cliente poderar realizar agendamentos pelo celular ou computador.

### 🔧 Instalação e configuração

# Primeiro, instale as dependencias listadas abaixo, pois são necessarias para executar o projeto:

## Comandos e ferramentas utilizadas no Setup do projeto:

## Next JS

Para realizar a instalação do NextJS, execute:
```
npx create-next-app@latest
```
* Coloque o nome do seu projeto: `nomeprojeto`
* Marque sim para usar o TypeScript:  Yes
* Marque sim para usar o ESLint?  Yes
* Marque sim para usar o Tailwind CSS? Yes
* Marque não para criar `src/` directory? No
* Marque sim para usar App Router? (recommended) Yes
* Marque sim para usar `next dev`?  No / Yes
* Marque não em import alias (`@/*` by default)? Yes
* >> What import alias would you like configured? @/* No

## Prisma
** Para realizar a instalação do Prisma, execute:
```
npm install prisma --save-dev
```
Inicia o prista e informa que irá utilizar o `postgresql` como BD
```
npx prisma init --datasource-provider postgresql
```
*Será criado um arquivo .env onde tem o `Database_URL`, acesse o `Neondb` para pegar a URL e copiar dentro do .env
*Para migrar o banco criado em `./prisma/schema.prisma` execute:
```
npx prisma migrate dev --name init_db
```
* O comando acima vai criar uma migrations em modo de desenvolvimento
* Dentro de `package.json` insira : abaixo de `scripts`
```
"prisma": {
"seed": "ts-node prisma/seed.ts" }
```
* No arquivo dentro de ./prisma chamado `seed.ts` que popula o banco de dados, para conseguir rodar ele é necessario instalar o `ts-node` com comando:
```
npm install -D ts-node
```
Depois execute:
```
npx prisma db seed
```
(O comando acima executa o Script dentro de Seed.ts)

## Prettier
```
npm install -D prettier prettier-plugin-tailwindcss
```
Após a instalação :
* Crie na pasta raiz um arquivo chamado .prettierrc.json e insira :
```
{
"plugins": [
"prettier-plugin-tailwindcss"
],
"tabWidth": 2,
"semi": false
}
```
## Shadcn.ui
```
npx shadcn-ui@latest init
```
O comando a cima cria as pastas ./lib e ./components  (caso ele não crie a componets, ele cria quando você instalar algum componente disponibilizado no site do shadcn)
em components.json você configura o caminho

## 🛠️Após instalar todas as dependencias, execute o comando abaixo para inciar:
```
npm run dev
```
Abra [http://localhost:3000](http://localhost:3000) com seu navegador para visualizar a pagina.
## ✒️ Autores

* **Arlan** - *Desenvolvimento* - [ArlanD3v](https://github.com/ArlanD3v/)
* **Felipe Rocha** - *Mentor* - [Felipe](https://github.com/felipemotarocha)
