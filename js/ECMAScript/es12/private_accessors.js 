// Let's create a class named Str.
class Str {
    // The private attributes can be created by prepending '#'
    // before the attribute name.
    #uniqueStr;

    constructor() {}

    // A private Setters can be created by prepending '#' before
    // the Setter name.
    set #generateUniqueStringByCustomLength(length = 24) {
        const characters = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789";
        let randomStr = "";

        for (let i = 0; i < length; i++) {
            const randomNum = Math.floor(Math.random() * characters.length);
            randomStr += characters[randomNum];
        }

        this.#uniqueStr = randomStr;
    }

    // Public Setter
    set setRandomString(length) {
        this.#generateUniqueStringByCustomLength = length;
    }

    // A private getter can be created by prepending '#' before
    // the Getter name.
    get #fetchUniqueString() {
        return this.#uniqueStr;
    }

    // Public Getter
    get getRandomString() {
        return this.#fetchUniqueString;
    }
}

const str = new Str();
// Calling a public Setter which will then access the private Setter
// within the class.
str.setRandomString = 20;

// Calling a public Getter which will then access the private Getter
// withing the class.
const uniqueStr = str.getRandomString;
console.log(uniqueStr); // This will print a random string everytime you execute the Getter after the Setter.