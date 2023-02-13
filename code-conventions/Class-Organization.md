# Class Organization

Classes should be organized with the reader in mind rather than the writer. Since most readers will be using the public interface of the class

Source files should contain only one public type, although multiple internal classes are allowed.

Source files should be given the name of the public class in the file.

Organize namespaces with a clearly defined structure,

Class members should be alphabetized, and grouped into sections:

- Constant Fields
- Static Fields
- Fields
- Constructors
- Properties
- Events / Delegates
- LifeCycle Methods (Awake, OnEnable, OnDisable, OnDestroy)
- Public Methods
- Private Methods
- Nested types

Within each of these groups order by access:
- public
- serializedFields
- internal
- protected
- private

The only exception is serialized or public UnityEvent which should always be declared under everything else.
this is to make the inspector more organized.

```csharp
namespace ProjectName
{
	/// <summary>  
	/// Brief summary of what the class does
	/// </summary>
    public class Account
    {
      [Tooltip("Public variables set in the Inspector, should have a Tooltip")]
      public static string BankName;
      
	  /// <summary>  
	  /// They should also have a summary
	  /// </summary>
      public static decimal Reserves;
 
      public string BankName;
      public const string ShippingType = "DropShip";
      
      private float _timeToDie;
      
      // UnityEvents should always be defined last. this is to make the editor look more readable.
      public UnityEvent onOpened = new();
      public UnityEvent onClosed = new();
	 
      public string Number {get; set;}
      public DateTime DateOpened {get; set;}
      public DateTime DateClosed {get; set;}
      public decimal Balance {get; set;}
            
      public Awake()
      {
        // ...
      }
      
      #endregion
	  #region Public Methods
	  
      public AddObjectToBank()
      {
        // ...
      }
    }
}
```


### Scripting Templates
To save some time you can overwrite Unity's default script template with your own to automatically setup the namespace and regions etc. See this Unity [support](https://support.unity3d.com/hc/en-us/articles/210223733-How-to-customize-Unity-script-templates) article to learn how.

### Namespace

Use a namespace to ensure your scoping of classes/enum/interface/etc won't conflict with existing ones from other namespaces or the global namespace. The project should at minimum use the projects name for the Namespace to prevent conflicts with any imported Third Party assets.

### All Public Functions Should Have A Summary
Simply, any function that has an access modifier of Public should have its summary filled out.
```csharp
/// <summary>
/// Fire a gun
/// </summary>
public void Fire()
{
// Fire the gun.
}
```

### Commenting
Comments should be used to describe intention, algorithmic overview, and/or logical flow. It would be ideal if from reading the comments alone someone other than the author could understand a function’s intended behavior and general operation.

While there are no minimum comment requirements and certainly some very small routines need no commenting at all, it is hoped that most routines will have comments reflecting the programmer’s intent and approach.

### Comment style

Place the comment on a separate line, not at the end of a line of code.

Begin comment text with an uppercase letter.

End comment text with a period.

Insert one space between the comment delimiter (//) and the comment text, as shown in the following example.

The // (two slashes) style of comment tags should be used in most situations. Where ever possible, place comments above the code instead of beside it. Here are some examples:

```csharp
        // Sample comment above a variable.
        private int _myInt = 5;
```

### Spacing
Do use a single space after a comma between function arguments.

Example: Console.In.Read(myChar, 0, 1);

- Do not use a space after the parenthesis and function arguments.
- Do not use spaces between a function name and parenthesis.
- Do not use spaces inside brackets.