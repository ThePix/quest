A list of translations needed for the Italian version of Quest
-------------------------------------------------------------

To support the AGAIN command, the command and abbreviation, plus an error message:

    again
    g
    There is nothing to repeat.

This is used in the status panel; not sure why it is missing, it has been in Quest for years:

    Status
    Score
    Health
    Money

Text for the interface:

    Type here...
    Continue...

Various error messages for when the player uses ALL.


    Nothing here to take.
    You've nothing to drop.
    You've nothing to wear.
    You've nothing to take off.

Possessives (the last three are netrual, male, female; all the same in English):

    its
    his
    her
    your
    their
    their
    their

For a list when there is nothing there:

    nothing

When the player locks a container:

    Locked.

When saying who the author is:

    by

Also:

    Eat
    Yes
    No


Various messages for clothing (object.article will be "it" or "them" in English):

    "You put " + object.article + " on."
    "You can't wear " + object.article + "."
    "You would need to get " + object.article + " before you can put " + object.article + " on."
    "You would need to get " + object.article + " before you can take " + object.article + " off."
    "You are already wearing " + object.article + "."
    "You are not wearing " + object.article + "."
    "You cannot remove " + object.article + "!"
    "You cannot wear that over " + GetDisplayGarment(object) + "."
    "You cannot wear that while wearing " + GetDisplayGarment(object) + "."
    "You take " + object.article + " off."
    "You can't remove that while wearing " + GetDisplayGarment(object) + "."

And for containers:

    "You can't put " + object.article + " there."
  
This is added to an item when it is listed (eg "hat (worn)")  
  
    worn

Also these used for display verbs (when you click on an object, these are shown and can be clicked):

    Wear
    Remove

Commands are tricky because we need to cover all possibilities, so please list any alternatives you can think of in the format "take #object# off".

    wear #object#
    remove #object#
    give #object#
    tell #object1# to #object2#
  

These error responses are also a bit more tricky as they vary depending on the object. The WriteVerb function modifies the verb, so in the first, it might return "They are". This will work in Italian too.

    WriteVerb(object, "be") + " too heavy to be taken."
    "You can't carry any more items."
    "You can't put more items in " + object.article + "."

    "You can't put " + object.article + " there."
    "You can't give " + object.article + "."
    "You eat " + object.article + "."
    "It is too dark to make anything out."
    WriteVerb(object, "do") + " nothing."


