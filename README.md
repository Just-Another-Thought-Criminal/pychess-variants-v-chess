## [www.pychess.org](https://www.pychess.org)

[![Python-CI](https://github.com/gbtami/pychess-variants/actions/workflows/ci.yml/badge.svg)](https://github.com/gbtami/pychess-variants/actions/workflows/ci.yml)
[![Nodejs-CI](https://github.com/gbtami/pychess-variants/actions/workflows/nodejs.yml/badge.svg)](https://github.com/gbtami/pychess-variants/actions/workflows/nodejs.yml)

pychess-variants is a free, open-source chess server designed to play chess variants. I would like to code my variant of chess and submit it as a
supported variant on pychess. others are welcome to help.

v-chess is an expansion of crazyhouse, capahouse, s-house, and grandhouse, and placement chess. there are some new pieces we are going to add: just as the chancellor is a combination of rook and knight, and the archbishop is a combination of bishop and knight, we can combine the pawn with the knight, the bishop, the rook, or the king or queen; and we can combine the knight with the king, and the knight again (knight squared).
the mounted pawn moves like a pawn but can also leap forward only.
the pawn-bishop combination is a cleric and can move on the diagonal without attacking, and otherwise moves like a pawn
the pawn-rook combination is a guard and can move and attack sideways but not move backwards, and otherwise moves like a pawn
the mounted king can move like a king and like a knight, and is able to leap over a rank or file where he otherwise would be in check; provided the square he moves to is not threatened. this only applies when he moves like a knight, i.e. the king cannot move into check as one might expect.
the pawn crosses with the queen is the princess and can move 2 squares in any direction; and the pawn crossed with the king is the prince and moves like a king. the knight-knight is the knightrider and can move like a knight successively any single direction as many times as he wants on unobstructed ground, he may leap like a knight once at the beginning of the movement.
the idea here is that the king is more difficult to mate because of his mount; the extra space on a grandhouse board can be filled with these additional major and minor pieces; the cleric and guard work with the knights, bishop, and pawns to provide troops for the army; the major pieces represent special formations for offense or defense; and the prince and princess help to create a bodyguard for the king.
in terms of incorporating placement chess, it would be nice to start with the option of having some pieces in the pocket indefinitely rather than on the board.

Currently supported games are:

- [Makruk](https://www.pychess.org/variants/makruk)
- [Makpong](https://www.pychess.org/variants/makpong)
- [Ouk Chatrang](https://www.pychess.org/variants/cambodian)
- [Sittuyin](https://www.pychess.org/variants/sittuyin)
- [ASEAN Chess](https://www.pychess.org/variants/asean)
- [Shogi](https://www.pychess.org/variants/shogi)
- [Minishogi](https://www.pychess.org/variants/minishogi)
- [Kyoto shogi](https://www.pychess.org/variants/kyotoshogi)
- [Dobutsu shogi](https://www.pychess.org/variants/dobutsu)
- [Goro-Goro shogi](https://www.pychess.org/variants/gorogoro)
- [Tori Shogi](https://www.pychess.org/variants/torishogi)
- [Xiangqi](https://www.pychess.org/variants/xiangqi)
- [Manchu](https://www.pychess.org/variants/manchu)
- [Janggi](https://www.pychess.org/variants/janggi)
- [Minixiangqi](https://www.pychess.org/variants/minixiangqi)
- [Placement chess](https://www.pychess.org/variants/placement)
- [Crazyhouse](https://www.pychess.org/variants/crazyhouse)
- [Atomic](https://www.pychess.org/variants/atomic)
- [S-chess](https://www.pychess.org/variants/seirawan)
- [Capablanca](https://www.pychess.org/variants/capablanca)
- [Gothic](https://www.pychess.org/variants/gothic)
- [Grand](https://www.pychess.org/variants/grand)
- [Shako](https://www.pychess.org/variants/shako)
- [Shogun](https://www.pychess.org/variants/shogun)
- [Orda](https://www.pychess.org/variants/orda)
- [Synochess](https://www.pychess.org/variants/synochess)
- [Hoppel-Poppel](https://www.pychess.org/variants/hoppelpoppel)
- [Shinobi](https://www.pychess.org/variants/shinobi)
- [Empire Chess](https://www.pychess.org/variants/empire)
- [Orda Mirror](https://www.pychess.org/variants/ordamirror)
- [Chak](https://www.pychess.org/variants/chak)
- [Chennis](https://www.pychess.org/variants/chennis)
- [S-house (S-chess+Crazyhouse)](https://www.pychess.org/variants/shouse)
- [Capahouse (Capablanca+Crazyhouse)](https://www.pychess.org/variants/capahouse)
- [Grandhouse (Grand chess+Crazyhouse)](https://www.pychess.org/variants/grandhouse)
- [Chess](https://www.pychess.org/variants/chess)

Additionally you can check Chess960 option in for Chess, Crazyhouse, Atomic, S-chess, Capablanca and Capahouse to start games from random positions with 
[Chess960 castling rules](https://en.wikipedia.org/wiki/Fischer_random_chess#Castling_rules)

For move generation, validation, analysis and engine play it uses
- [Fairy-Stockfish](https://github.com/ianfab/Fairy-Stockfish)
- [fairy-stockfish.wasm](https://github.com/ianfab/fairy-stockfish.wasm)
- [fairyfishnet](https://github.com/gbtami/fairyfishnet) fork of [fishnet](https://github.com/lichess-org/fishnet)
- [lichess-bot-variants](https://github.com/gbtami/lichess-bot-variants) fork of [lichess-bot](https://github.com/ShailChoksi/lichess-bot)

On client side it is based on
[chessgroundx](https://github.com/gbtami/chessgroundx) fork of [chessground](https://github.com/lichess-org/chessground)

##

As you know, pychess-variants is a free server and it will remain free forever. However, maintaining and improving the server costs time and money.

If you like our work and find our server useful, please donate through [patreon](https://www.patreon.com/pychess) or directly through [paypal](https://www.paypal.me/gbtami)!!
Your contribution will be greatly appreciated and help me continue to develop this awesome server.

## Installation

### Prerequisites
* You need mongodb up and running. [Mongo daemon](https://www.mongodb.com/docs/manual/installation/)


### Project setup
```
pip3 install -r requirements.txt --user // Install python requirements
yarn install                            // Install node requirements
yarn dev                                // Compile typescript files to javascript
yarn md                                 // Compile md files to html
```

### Start server
```
python3 server/server.py
```

## Supported browsers

Pychess-variants should support almost all browsers. Though older browsers (including any version of Internet Explorer) will not work. For your own sake, please upgrade. Security and performance, think about it!

Only [Fairy-Stockfish analysis](https://www.pychess.org/analysis/chess) might not work on all browsers.
