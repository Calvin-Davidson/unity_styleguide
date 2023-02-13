## Variables
The words `variable` and `property` may be used interchangeably.

#### Variable Naming
##### Nouns
All non-boolean variable names must be clear, unambiguous, and descriptive nouns.

##### case
All variables use PascalCase unless marked as private which use camelCase.

Use PascalCase for abbreviations of 4 characters or more (3 chars are both uppercase).

##### Considered Context
All variable names must not be redundant with their context as all variable references in the class will always have context.

###### Considered Context Examples:
Consider a Class called PlayerCharacter.

**Bad**

- PlayerScore
- PlayerKills
- MyTargetPlayer
- MyCharacterName
- CharacterSkills
- ChosenCharacterSkin

All of these variables are named redundantly. It is implied that the variable is representative of the PlayerCharacter it belongs to because it is PlayerCharacter that is defining these variables.

**Good**

- Score
- Kills
- TargetPlayer
- Name
- Skills
- Skin

##### Variable Access Level
In C#, variables have a concept of access level. Public means any code outside the class can access the variable. Protected means only the class and any child classes can access this variable internally. Private means only this class and no child classes can access this variable. Variables should only be made public if necessary.

Prefer to use the attribute `[SerializeField]` instead of making a variable public.

Local Variables
Local variables should use camelCase.

###### Implicitly Typed Local Variables
Use implicit typing for local variables when the type of the variable is obvious from the right side of the assignment, or when the precise type is not important.

```csharp
var var1 = "This is clearly a string.";
var var2 = 27;
var var3 = Convert.ToInt32(Console.ReadLine());
// Also used in for loops
for (var i = 0; i < bountyHunterFleets.Length; ++i) {};
```

Do not use var when the type is not apparent from the right side of the assignment. Example

```csharp
int var4 = ExampleClass.ResultSoFar();
```

Private Variables
Private variables should have a prefix with a underscore `_myVariable` and use camelCase.

Unless it is known that a variable should only be accessed within the class it is defined and never a child class, do not mark variables as private. Until variables are able to be marked `protected`, reserve private for when you absolutely know you want to restrict child class usage.

##### Do Not use Hungarian notation
Do not use Hungarian notation or any other type identification in identifiers

```csharp
// Correct
int counter;
string name;

// Avoid
int iCounter;
string strName;
```

##### Variables accessible in the Editor
###### Tooltips
All [Serializable](https://github.com/justinwasilenko/Unity-Style-Guide/blob/master/README.md#serializable) variables should have a description in their [Tooltip] fields that explains how changing this value affects the behavior of the script.

###### Variable Slider And Value Ranges
All [Serializable](https://github.com/justinwasilenko/Unity-Style-Guide/blob/master/README.md#serializable) variables should make use of slider and value ranges if there is ever a value that a variable should not be set to.

Example: A script that generates fence posts might have an editable variable named PostsCount and a value of -1 would not make any sense. Use the range fields `[Range(min, max)]` to mark 0 as a minimum.

If an editable variable is used in a Construction Script, it should have a reasonable Slider Range defined so that someone can not accidentally assign it a large value that could crash the editor.

A Value Range only needs to be defined if the bounds of a value are known. While a Slider Range prevents accidental large number inputs, an undefined Value Range allows a user to specify a value outside the Slider Range that may be considered 'dangerous' but still valid.

#### Variable Types
##### Booleans
###### Boolean Prefix
All booleans should be named in PascalCase but prefixed with a verb.

Example: Use isDead and hasItem, not Dead and Item.

###### Boolean Names
All booleans should be named as descriptive adjectives when possible if representing general information.

Try to not use verbs such as isRunning. Verbs tend to lead to complex states.

###### Boolean Complex States
Do not use booleans to represent complex and/or dependent states. This makes state adding and removing complex and no longer easily readable. Use an enumeration instead.

Example: When defining a weapon, do not use isReloading and isEquipping if a weapon can't be both reloading and equipping. Define an enumeration named WeaponState and use a variable with this type named WeaponState instead. This makes it far easier to add new states to weapons.

Enums
Enums use PascalCase and use singular names for enums and their values. Exception: bit field enums should be plural. Enums can be placed outside the class space to provide global access.

Example:

```csharp
public enum WeaponType
{
Knife,
Gun
}

// Enum can have multiple values
[Flags]
public enum Dockings
{
None = 0,
Top = 1,
}

public WeaponType Weapon
```

##### Arrays
Arrays follow the same naming rules as above, but should be named as a plural noun.

Example: Use `Targets`, `Hats`, and `EnemyPlayers`, not `TargetList`, `HatArray`, `EnemyPlayerArray`.

##### Interfaces
Interfaces are led with a capital I then followed with PascalCase.

Example: `public interface ICanEat { }`

