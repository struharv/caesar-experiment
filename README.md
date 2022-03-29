# caesar-experiment
Road editing software: http://www.openjump.org/


----
Structure of the simulation:
- intersection
  - action initialize
  - action compute_crossing
  - action to_green
  - action to_red
  - reflex dynamic_node when: is_traffic_signal
  - aspect default
- road
  - aspect default
- people
  - reflex breakdown when: flip(proba_breakdown)
  - reflex time_to_go when: final_target = nil
  - reflex move when: current_path != nil and final_target != nil
  - aspect default
       

action:
- action is a function or procedure run by an instance of species

reflex:
- reflex is a procedure that is executed in each step

aspect:
- aspect allows you to define how you want your species to be represented in the simulation


## What do we need 
![](figure-overview.png)



- Intersection always in red 
    - random (at first)
    - priority roles 
    
- calculate cars that are close to the intersection, which will enter the negotiation round
    - speed of the car? 
    - remaining time?

- communication
