# AIBehaviour

Add these components to create a waypoint patroling and chasing system to create a simple AI enemy behaviour.
A simple movement behaviour is also added but not needed for the rest of the components to work by themselves.

## Contents

This component is made from the following behaviours:
- `AI`
- `Movement`

And the following states:
- `Chase`
- `Patrol`
- `GenerateEnemies`
- `SimpleMovement`

### Chase

When added to an object, this component manages the chasing range. This state retains a target, when the target is not within range, it will remain static and when the target is within range, it will become mobile and follow the target. In order for it to work, when this component is added to an enemy, the target and the move speed must be entered into the inspector.

### Patrol

When added to an object, this component finds a path of waypoints located around the scene. These can be found as ``WayPoint`` in the project examples.The object will navigate through them and follow the order we state. By dragging ``Waypoint`` objects into the scene and dragging each one of them inside the component, under the inspector. The order in which we place them will determine the specific route followed by the object.

### GenerateEnemies

When added to an object, this state spawns objects at regular intervals which will switch to the ``Chase`` state when the target is again within range. For this to work, an empty game object should be added to the scene and then attaching this component to it. On the inspector, the target must be stated. The speed these objects spawn can be changed under the ``WaitForSeconds`` function.


### SimpleMovement

When added to an object, this state manages its movement, directions and speed. Speed can be adjusted under the component details in the inspector. 


