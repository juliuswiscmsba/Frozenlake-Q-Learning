### Frozenlake-Q-Learning

#### Frozen lake (from Open AI: https://www.gymlibrary.dev/environments/toy_text/frozen_lake/)

![frozen_lake](https://user-images.githubusercontent.com/90480106/208994798-790c5ec6-c3e4-46e9-8433-becabfad58be.gif)

Frozen lake involves crossing a frozen lake from Start(S) to Goal(G) without falling into any Holes(H) by walking over the Frozen(F) lake. The agent may not always move in the intended direction due to the slippery nature of the frozen lake.

##### Action Space

The agent takes a 1-element vector for actions. The action space is (dir), where dir decides direction to move in which can be:

  * 0: LEFT

  * 1: DOWN

  * 2: RIGHT

  * 3: UP

##### Observation Space

The observation is a value representing the agent’s current position as current_row * nrows + current_col (where both the row and col start at 0). For example, the goal position in the 4x4 map can be calculated as follows: 3 * 4 + 3 = 15. The number of possible observations is dependent on the size of the map. For example, the 4x4 map has 16 possible observations.

##### Rewards
 
  * Reach goal(G): +1

  * Reach hole(H): 0

  * Reach frozen(F): 0

#### Q Learning

Apply Q Learning to update the Q table.

<img width="744" alt="Screenshot 2022-12-21 at 2 17 11 PM" src="https://user-images.githubusercontent.com/90480106/208995387-ade2109a-1698-4530-81e6-21c5103e1540.png">
