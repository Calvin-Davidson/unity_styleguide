## 3.4 Functions, Events, and Event Dispatchers
This section describes how you should author functions, events, and event dispatchers. Everything that applies to functions also applies to events, unless otherwise noted.

##### Function Naming
The naming of functions, events, and event dispatchers is critically important. Based on the name alone, certain assumptions can be made about functions. For example:

- Is it a pure function?
- Is it fetching state information?
- Is it a handler?
- What is its purpose?

These questions and more can all be answered when functions are named appropriately.


All Functions Should Be Verbs
All functions and events perform some form of action, whether its getting info, calculating data, or causing something to explode. Therefore, all functions should start with verbs. They should be worded in the present tense whenever possible. They should also have some context as to what they are doing.

**Good examples:**

- Fire - Good example if in a Character / Weapon class, as it has context. Bad if in a Barrel / Grass / any ambiguous class.
- Jump - Good example if in a Character class, otherwise, needs context.
- Explode
- ReceiveMessage
- SortPlayerArray
- GetArmOffset
- GetCoordinates
- UpdateTransforms
- EnableBigHeadMode
- IsEnemy - "Is" is a verb.

**Bad examples:**

- Dead - Is Dead? Will deaden?
- Rock
- ProcessData - Ambiguous, these words mean nothing.
- PlayerState - Nouns are ambiguous.
- Color - Verb with no context, or ambiguous noun.

##### Functions Returning Bool Should Ask Questions
When writing a function that does not change the state of or modify any object and is purely for getting information, state, or computing a yes/no value, it should ask a question. This should also follow the verb rule.

This is extremely important as if a question is not asked, it may be assumed that the function performs an action and is returning whether that action succeeded.

**Good examples:**

- IsDead
- IsOnFire
- IsAlive
- IsSpeaking
- IsHavingAnExistentialCrisis
- IsVisible
- HasWeapon - "Has" is a verb.
- WasCharging - "Was" is past-tense of "be". Use "was" when referring to 'previous frame' or 'previous state'.
- CanReload - "Can" is a verb.

**Bad examples:**
- Fire - Is on fire? Will fire? Do fire?
- OnFire - Can be confused with event dispatcher for firing.
- Dead - Is dead? Will deaden?
- Visibility - Is visible? Set visibility? A description of flying conditions?
- Event Handlers and Dispatchers Should Start With On
- Any function that handles an event or dispatches an event should start with On and continue to follow the verb rule.

**Good examples:**

- OnDeath - Common collocation in games
- OnPickup
- OnReceiveMessage
- OnMessageRecieved
- OnTargetChanged
- OnClick
- OnLeave
  **Bad examples:**

- OnData
- OnTarget