# Diplomacy

## War

### Starting war

A town/duchy/... can declare war to another entity. Action is onesided. Both attacker and defender when in war have option to call in their parent entity (town -> duchy -> kingdom -> empire). Parent can refuse the call. If parent accepts, then it becomes war of parent vs. enemy town. When parent declares war, it can call all of its children into war, and they can refuse or accept.

### Ending war

War is ended through peace treaty. This is functionality that enables certain post-war actions. Leader of each side can send peace treaty to any member of the opposing side (leader to leader --> ends whole war, leader to town --> ends war for that town)

#### Peace treaty

In peace treaty the sender can specify which regions will be transferred to who, amount of money sent from one to another, change allegiance (transfer town from one kingdom to another). The recipient gets treaty and can either accept (ends war and enforces actions specified in it) or refuse (war continues).

##### Occupation period

One of peace treaty terms can be occupation period. This gives temporarily control of losing towns to winner. This can be used to enforce non-automatic terms (like paying reparations in material items)