# Comms Clockin

Super basic Discord bot that allows clocking in and out of various "masks" and importing that data into other places such as Google Sheets.

## Infra

- node.js
- discord.js
- prisma with postgresql
- pain and suffering

## How to Host

1. make sure node.js is installed, optionally also install yarn (`npm i -g yarn`)
2. make sure you have a postgresql server *somewhere*, either locally or running somewhere else
3. clone this repo (`git clone https://github.com/glitchmasta47/commsclockin.git/`)
4. set your postgresql connection credentials in a `.env` file, using the template in `.env.example`
5. run `yarn` (or `npm i`)
6. push the database schema to your postgresql instance (`prisma db push` or `yarn prisma db push`)
7. run `yarn start` (or `npm start`)

## How to Use

*Thank you Discord for forcing slash commands. :)*

You can view all commands by typing a `/` in chat and looking for them under "Comms Clockin" (or whatever your bot was named in the Discord developer panel).

- `/clockin [mask]` - clocks in to one of the masks, or the default mask is no mask is given
- `/clockout [mask]` - clocks out of one of the masks, or the default mask is no mask is given
- `/data [user]` - shows data for a user, or yourself if no user is given
- `/export` - exports the data of every user in the server and sends it to you via DM
- `/setup` - in-discord setup menu for the bot