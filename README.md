# Project Jetpack Journey

Developed with Unreal Engine 5.6.0

Based on the course Unreal Engine 5 Blueprints - The Ultimate Developer Course by Stephen Ulibarri  

Jetpack Journey is a third-person 3D platformer where the player controls a character equipped with a jetpack, navigating through floating platforms in a sci-fi-inspired environment. The player must carefully manage jet fuel, avoid falling, and ultimately reach a pressure plate that signals victory. Along the way, dynamic platforms, color-changing collectibles, and an intuitive user interface create a complete gameplay loop.  

Key Features Implemented  
  
Advanced Player Movement
* Jetpack-powered both jumps and hovering
* Fuel consumption and recharge system
* Fall detection and respawn logic

Animation System  
* Integrated third-person character animation blueprint
* State-driven transitions between:  
  * Idle  
  * Walking  
  * Running  
  * Jetpack hovering / flying  

Platforming Mechanics
* Rotating and moving platforms with timed behavior (Floating and PingPong)
* Environmental hazards (fall zones, platform gaps)

Interactive Objects  
* Collectible fuel pickups with dynamic placement logic
* Pressure plates triggering level win events

Gameplay Progression  
* Win and lose conditions handled through Blueprint event flow  
* End-game UI displayed based on result (victory or failure)  

End Game Menu Widget  
* Dynamically loaded widget for victory/defeat screen
* Event dispatchers used for clean separation between UI and game logic
* Options to replay the level or quit the game
* Input mode and mouse cursor management via Player Controller

Procedural Blueprint Logic  
* Jet fuel collectibles change color based on their environment:
* All driven via Construction Script and line traces

Clean Architecture  
* Usage of functions, macros, event dispatchers, and soft references
* Input and UI state handled in the Player Controller
* Reusable widget logic encapsulated in Blueprint classes

Technologies Used  
* Unreal Engine 5.6
* Blueprints Visual Scripting
* UI Widgets (UMG)
* Player Controller and Pawn architecture
* Construction Script for editor-time logic
* Line tracing and collision channels

Gameplay Flow  
* Player navigates a platforming level using jetpack mechanics.
* Collectibles and interactive elements modify the experience.
* Upon falling or winning, an end-game menu appears with options.
* Game logic is cleanly separated from UI via delegates and controller-based input mode switching.

Chaos Vehicle System (UE5)
* Fully Drivable Vehicle using WheeledVehiclePawn
* Physics-Based Suspension and Torque System powered by Chaos Physics
* Vehicle-Specific Animation Blueprint using WheelController node
* Modular Blueprints for front wheels, rear wheels, vehicle mesh, and logic
* Controls:  
  * W / Right Trigger – Accelerate
  * S / Left Trigger – Brake or Reverse
  * Space / Gamepad Face Button – Handbrake
  * A / D – Steer left/right
  * Mouse / Right Stick – Look around
