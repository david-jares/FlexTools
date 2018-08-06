# FlexTools
A Combination of Tools for Unity - it is Work in Progress and not yet finished

Dependencies :
  Odin - Serializer, https://github.com/TeamSirenix/odin-serializer
  Paradaxnotions - Flowcanvas & Nodecanvas :   http://www.paradoxnotion.com/    

Features :
  Inversion of Cotrol, Dependency Injection, Shared Variables & Events, 
  Easier Debugging of eentbased flows and sared VariableManipulations.

Variables and GameEvents can be created as ScriptableObject-Dependencies
They can be listened to and they can be raised
Whenever a change occurs, all listeners will be notified
This is heavily based on http://www.roboryantron.com/2017/10/unite-2017-game-architecture-with.html and reuses core parts of his repository on https://github.com/roboryantron/Unite2017. Everything is refactored into the namespace "Flex" to keep it short and simple. 

New Types of Variables and GameEvents can be done by Subclasssing FlexVariable<T> or GameEvent<T> . 
(GameEvent is itself a Subclass of FlexVariable ).
When doing this, also a complementing Script subclassing from FlexVariableReference<T> should be Created. 
These References can then be used in your own scripts as neat Holders of Varaiables and can be switched to.
Also , in the Editorscript FlexReferenceDrawer should be extended with  [CustomPropertyDrawer(typeof(YoutnewFlexVariableReferenceType))] to support the cool drawing.
Gameevents can be debuuged by attaching a MyEventVisualizer.cs as a component to aan Object with a FlowscriptController
