# Game of War: 2-player card console game

Game of War is a card game in which players play their random cards from their respective parts of the deck to see which hand is larger. The game is built for the user to play directly from the console using object-oriented programming.

Assigned from:
[GA users only](https://git.generalassemb.ly/dc-wdi-fundamentals/game-of-war)

## How to Play

To play, each player reveals the top card in their stack. The player who played the card with the higher rank takes both cards and puts them at the bottom of their stack in an arbitrary order. If there is a tie, then it’s WAR! In the card game each player adds places the top three cards of their stack face down, and then each player reveals the top card again. Whoever wins out of the second reveal takes all of the cards, and if there is another tie the process repeats until there is a winner.

### Prerequisites to Build

Requirements for the software and other tools to build, test and push 
- [Javascript Objects and Classes](https://git.generalassemb.ly/dc-wdi-fundamentals/objects-intro)
- [Object Oriented Programming](https://git.generalassemb.ly/dc-wdi-fundamentals/javascript-oop/blob/master/object-oriented-javascript.md)

## Object Oriented Programming


### Classes and Instances
We use methods to initialize, modify, or act on an objects' internal state.
Because these methods will be the same across all instances of a type of object, we define a single class with all of this behavior described in one place.
We then use that class to instantiate as many instances (objects) of the class as we need.
Constructors are special methods that will be invoked whenever we create a new instance of our class. If our class is what defines our template, the constructor method is what fills it in for a particular instance.

### Constructors

Constructors are special methods that will be invoked whenever we create a new instance of our class. If our class is what defines our template, the constructor method is what fills it in for a particular instance.
Here is an example of how a constructor is used to code the game: 

       constructor(cards = newDeck()) {
        this.cards = cards;
      };
### Attributes
If we want to create our own classes, all we need is a name for our class and a definition of the information and behavior we want to encapsulate in our class. The information and behavior we want to describe with our class has a special name: an attribute. There are two kinds of attributes: data attributes and procedural attributes (more commonly called methods).

### Methods
Methods are the "functions of Classses" used methods to initialize, modify, or act on an objects' internal state. For example:
Here's an example of how methods can be used in a class in the Game of War.

    shuffle () {
      for (let i = this.numberOfCards - 1; i > 0; i--) {
          const newIndex = Math.floor(Math.random() * (i + 1))
          const oldValue = this.cards[newIndex]
          this.cards[newIndex] = this.cards[i]
          this.cards[i] = oldValue;
      };
    };

## Review!

Object oriented programming gives use three major benefits:

> (1) Encapsulation: The complexity of our objects is hidden and a user can interact with a well defined set of methods. We can redefine internal behavior without changing anything externally - a huge benefit for refactoring.
(2) Modularity: Because the interface (set of methods) for an object is well defined, it is easy to exchange one object for another and reorganize objects without breaking them.
(3) Inheritance: Object Oriented design lets certain classes inherit from, or borrow the behavior of another, more general class. The inheriting class can add and overwrite inherited methods.

## Built With

  - [Contributor Covenant](https://www.contributor-covenant.org/) - Used
    for the Code of Conduct
  - [Creative Commons](https://creativecommons.org/) - Used to choose
    the license

## Versioning

We use [Semantic Versioning](http://semver.org/) for versioning. For the versions
available, see the [tags on this
repository](https://github.com/PurpleBooth/a-good-readme-template/tags).

## Authors

  - **Billie Thompson** - *Provided README Template* -
    [PurpleBooth](https://github.com/PurpleBooth)


## Acknowledgments

  - Hat tip to anyone whose code is used
  - Inspiration
  - etc
