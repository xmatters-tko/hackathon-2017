# xMatters TKO 2019 Coding Challenge

_July 11th, 2019 at Westin Hotel, Whistler._

![Battle Snake](docs/bs-logo-dark.png)

The 2019 xMatters TKO coding challenge will be BattleSnake! ...Again!!!

BattleSnake is an adaptation of the classic video game "Snake", where the player maneuvers a snake around the play field to collect food pellets, which makes the snake grow longer. The main objective is to collect as much food as as possible, while avoiding hitting obstacles, such as other snakes and most importantly - your own snake.

In BattleSnake, each round two snakes are pitted against each other, and the goal is to be the last snake left alive at the end of the round.

![Example Game Animation](docs/game.gif)

## Game rules

#### You lose if your snake…
* Runs off the board.
* Runs into another snake's body.
* Runs into its own body.
* Collides head-to-head with a longer snake (both die if they are of the same size).
* Starves.

#### Starvation rules
* Your snake starts out with 100 health.
* Snake loses 1 point on every turn.
* When your snake's health reaches 0, it dies of starvation.

#### Avoiding starvation
* Food pellets spawn randomly around the play field.
* Each food pellet increases your snake's length by 1.
* Each pellet resets your snake's health to 100.

## Game Server
We will be hosting a game server where the games will be played. The game server is the brain of the operations and coordinates all of the game play.
* Snakes are registered with the game server using a publicly accessible URL
* Server communicates to snake clients via HTTP requests
* Snake client responds to API commands requested by the server

## Snake End Points
The creators of the BattleSnake server, StemboltHQ, have provided documentation for the API calls that each snake is required to implement. Basically, all competing clients are expected to provide a web application that is available at a routeable URL that can respond to HTTP requests and provide a route to three end points:
* POST /start
* POST /move
* POST /end

All clients are expected to respond within 500ms of the server's initial request. Failing to respond before the timemout may result in the server choosing a random move for you. All responses are expected to have a 200 OK status code.

All the details are documented at [BattleSnake API Reference](https://stembolthq.github.io/battle_snake/)

## Game Play
There are a number of controllable variables on each game server but the following should be considered as part of your game strategy:
* Expect a variable size grid
* Only one food pellet
  * Food pellets will respawn once consumed, in random locations
* Response times should be under 500ms

## Pre-requisites
Every team must show up with a laptop and have the following software installed in order to use the provided start snakes.
* Docker  (https://www.docker.com/products/docker-desktop)
* Git CLI (https://git-scm.com/downloads)
* Heroku CLI (https://devcenter.heroku.com/articles/heroku-cli)
* Create a free account on Github - https://www.github.com/
* Create a free account on Heroku - https://www.heroku.com/


## Starter Snakes
We have provided a list of starter snakes that are Heroku ready, for javascript and java languages. Each project has a set of instructions on how to get it deployed and running on Heroku using the Git and Heroku command line tools.
Unlike the previous event the snakes are pre-programmed to seek out food so that you can jump into some more fun aspects right away 
* [xm-battlesnake-java](https://github.com/xmatters-tko/xm-battlesnake-java)
* [xm-battlesnake-nodejs](https://github.com/xmatters-tko/xm-battlesnake-nodejs)
* [xm-battlesnake-python](https://github.com/xmatters-tko/xm-battlesnake-python) python does not currently have a food seeking algorithm 

### Testing Your Snake
#### Curl your Snake
Like any web client, you can easily test your snake using curl which comes on most modern operating systems. The [BattleSnake API Reference](https://stembolthq.github.io/battle_snake/) has example curl commands for each end point you must implement.

#### Getting your own Game Server
Each team should run a game server locally to help iterate on your snake's AI. 
Game servers can be run on docker with: `docker run -it -p 4000:4000 stembolt/battle_snake`

## Team Registration
Every team are required their Snake URL before they can compete and scoring points! Registration is simple. Find Pete Kosa, given him your team name, and a working url of your snake. You cannot change the URL of your snake once registered. There's no time limit on registration can be done at any time prior to your first match.  

## Competition
the competition will be single elimination bracket of 16 teams 3-4 people per team :
* round of 16 - one match 
* round of 8 - one match
* semi final best 2 of 3
* final best 2 of 3

* 1st place 2000
* 2nd place 1000
* semi-finalists $500

the twelve first and second round losers will get places in a 3 match battle royale with the winner getting $1000

## Pro Tips
Each team will have people from different disciplines and skill sets. Work together as a team to ensure that everyone is involved in some capacity. Here are some tips on getting organized:
* Consider a team captain
  * someone to take on admin functions i.e. team registration, game submissions, coffee runs
* Get someone started immediately on working on server deplopyment for your snake
  * setting up the GitHub and Heroku accounts, forking the project, deploying to Heroku
* Break up development tasks
  * creating helper functions, laying out board strategy, figuring out testing
* Consider building mulitple snakes
  * divide and conquer by building several snakes and submitting the best one (only one can be submitted)

### Sportsmanship
The competition is intended to be fun and generate camaraderie with your fellow xPerts. There are plenty of examples and existing snakes on the internet. For obvious reasons these are off limits and defeat the purpose of the competition. So you will be competing based on the honor system.  We will not be able to police this as internet access is required to build and run your snake, However, if you are caught your snake will be disqualified from the competition. Play fair and keep it fun!
* Don't plagarize other snakes.
* No DDoSing your opponents.

## Getting Started
So what now!?
* Sign up for the free accounts
  * Install the pre-requisite CLI tools
* Pick a starter snake
  * Follow instructions
* Register your snake
  * use your team name
* Get coding!

## Asking for Help
We'll have a number of game officials that will be able to assist with getting the start snakes up and running, answering questions, helping on code reviews, etc. Call on anyone you see wearing the Red ball caps!
