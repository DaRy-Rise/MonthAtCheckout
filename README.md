# Month-at-checkout
This is the android game - simulator of cashier. Developed on the unity platform.
# Game description
A sarcastic old shopkeeper hires you as a cashier. You need to survive 30 in-game days. For each day you will receive an estimate: "A", "B", "C". If you get a "C" grade for 5 days in a row, the game ends.
The main responsibilities that the employer will reward you with: scan goods, manually enter the code in case of a bad barcode, give bags, check coupons for validity, reboot the system in case of an error, change the roll of checks, make sure that the child does not buy goods that are not for them, accept credit cards, or cash, give change. Each customer has his own limit of patience. Before each day you need to choose 1 of 6 cards. The resulting effect (positive or negative) will last for 1 day. The chance of getting a good card depends on how many misses you have made in the previous days.
# Gameplay Demo
![GameplayDemo](https://github.com/DaRy-Rise/Month-at-checkout/assets/64958256/0316ab8c-8af0-4d2c-8e75-94aa8a60c0c6)
![GameplayDemo2](https://github.com/DaRy-Rise/Month-at-checkout/assets/64958256/4fdecf57-097f-446d-86a1-ce9084e9ef05)
# Unity
* App works in full screen portrait mode. There is 4 scenes, between each implemented a loading screen through coroutines. 
* For card flip effect used DOTween package from Demigiant. 
* Also added a lot of animations and sounds. 
* App allows choose between two languages: english and russian. Also there is posibility to turn on and turn off the sound. Each *textmeshpro* object is assigned a script that allows, depending on the language settings, to read the desired text from the array.
* Prefabs are used for some objects in the scene (for example: products and customers parts are prefabs, instantiated by spawners and destroyed after uselessness). 
* All files are logically divided into folders. 
# Code
The code can be viewed in the folder *Assets/Scripts.* Writing style: camelCase. 
* The logic of objects is divided into different scripts. 
* Implemented writing and reading game data to json files. Game settings information is controlled by PlayerPrefs. 
* Singleton. General game and level information (stored in json) is read from a single class. 
* Created own enums
* Encapsulation is controlled not only by access modifiers, but also by attributes [HideInInspector] and [SerializeField]. Inheritance is used to bring common logic to the base class. Used out-of-the-box unity interfaces to implement some mechanics (such as drag and drop for products or swipe tracking for bag)
