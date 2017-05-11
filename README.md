# xMatters TKO 2017 Coding Challenge

_June 6-8th, 2017 at Hyatt Regency Vancouver._

![Battle Snake](docs/bs-logo-dark.png)

The 2017 xMatters TKO coding challenge will be BattleSnakes!

BattleSnake is an adaptation of the classic video game "Snake", where the player maneuvers a snake around the play field to collect food pellets, which makes the snake grow longer. The main objective is to collect as much food as as possible, while avoiding hitting obstacles, such as other snakes and most importantly - your own snake.

In BattleSnake, each round X number of snakes are pitted against each other, and the goal is to be the last snake left alive at the end of the round.

![Example Game Animation](docs/game.gif)

## Pre-requisites
Every team must show up with a laptop and have the following software installed:
* Git CLI (https://git-scm.com/downloads)
* Heroku CLI (https://devcenter.heroku.com/articles/heroku-cli)
* Create a free account on Heroku - https://www.heroku.com/

## Starter Snakes
We have provided a list of starter snakes that are Heroku ready, for the most common languages. Each project has a set of instructions on how to get it deployed and running on Heroku using the Git and Heroku command line tools.

* [xm-battlesnake-java](https://github.com/xmatters-tko/xm-battlesnake-java)
* [xm-battlesnake-nodejs](https://github.com/xmatters-tko/xm-battlesnake-nodejs)
* [xm-battlesnake-python](https://github.com/xmatters-tko/xm-battlesnake-python)
* [xm-battlesnake-go](https://github.com/xmatters-tko/xm-battlesnake-go)
* [xm-battlesnake-ruby](https://github.com/xmatters-tko/xm-battlesnake-ruby)
* [xm-battlesnake-clojure](https://github.com/xmatters-tko/xm-battlesnake-clojure)

## Testing Your Snake
#### Curl your Snake
Like any web client, you can easily test your snake using curl which comes on most modern operating systems. The [BattleSnake API Reference](https://stembolthq.github.io/battle_snake/) has example curl commands for each end point you must implement.

#### Game Tables
Each team will be given a game table to practice on once they provide a URL for their battle snake. The team game table can be used for testing your snake and making modifications. Your team game table will be assigned after you have successfully registered your team in Slack.

## API Documentation
The creators of the BattleSnake server, at StemboltHQ, have provided documentation for the API calls that each client is required to implement. Basically, all competing clients are expected to provide a web application that is available at a routeable URL that can respond to HTTP requests and provide a route to three end points:
* POST /start
* POST /move
* POST /end

All clients are expected to respond within 200ms of the server's initial request. Failing to respond before the timemout may result in the server choosing a random move for you. All responses are expected to have a 200 OK status code.

All the details are documented at [BattleSnake API Reference](https://stembolthq.github.io/battle_snake/)

## Team Registration
Any team can register through a Slack channel, #hackathon-2017, by using the following command:
```
tko register <team-name> <snake url>
```
This will add your team and it's snake to the list of participants. If you do not register, see @nick or @craig for help.

## Scoring
The competition will include a round robin tournament starting after the first hour, where each team will challenge all other teams to a head to head match. Every match should result in at least one team scoring a single point.
* In case of a draw, neither team scores a point
* Every team has the chance to score that same number of points

The competition will end with a battle royale single elimination tournament:
* Round One - Top 8 teams will be divided between four tables, last snake moves one to the second round
* Round Two - Top 4 teams will be divided between two tables, last snake moves one to the final round
* Final Round - top two snakes will go head to head until one snake wins
* First place wins 20 points, and the second place wins 10 points

## Game rules

#### You lose if your snake…
* Runs into another snake's body.
* Runs into its own body.
* Collides head-to-head with a longer snake (both die if they are of the same size).
* Starves.

#### Starvation rules
* Your snake starts out with 100 life and counts down by 1 each turn.
* When your snake's life total reaches 0, it dies of starvation.

#### Avoiding starvation
* Food pellets spawn randomly around the play field.
* Each food pellet increases your snake's length by 1 and resets its life to 100.

#### Sportsmanship
* No DDoSing your opponents.
* No manual control of your snake.

