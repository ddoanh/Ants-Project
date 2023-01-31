# Ants Project
![splash](https://user-images.githubusercontent.com/98563830/215884908-0aee7a6f-d024-4809-b167-9eea25b9304a.png)

## Files
<p>The <a href="ants.zip">ants.zip</a> archive contains several files
<ul>
  <li><code>ants.py</code>: The game logic of Ants Vs. SomeBees</li>
  <li><code>ants_gui.py</code>: The original GUI for Ants Vs. SomeBees</li>
  <li><code>gui.py:</code> A new GUI for Ants Vs. SomeBees.</li>
  <li><code>graphics.py</code>: Utilities for displaying simple two-dimensional animations</li>
  <li><code>utils.py</code>: Some functions to facilitate the game interface</li>
  <li><code>ucb.py</code>: Utility functions for CS88</li>
  <li><code>state.py</code>: Abstraction for gamestate for gui.py</li>
  <li><code>assets</code>: A directory of images and files used by <code>gui.py</code></li>
  <li><code>img</code>: A directory of images used by <code>ants_gui.py</code></li>
  <li><code>ok</code>: The autograder</li>
  <li><code>proj3.ok</code>: The <code>ok</code> configuration file</li>
  <li><code>tests</code>: A directory of tests used by <code>ok</code></li>
</ul>

## Description
A game of Ants Vs. SomeBees consists of a series of turns. In each turn, new bees may enter the ant colony. Then, new ants are placed to defend their colony. Finally, all insects (ants, then bees) take individual actions. Bees either try to move toward the end of the tunnel or sting ants in their way. Ants perform a different action depending on their type, such as collecting more food or throwing leaves at the bees. The game ends either when a bee reaches the end of the tunnel (you lose), the bees destroy the QueenAnt if it exists (you lose), or the entire bee fleet has been vanquished (you win).
![gui_explanation](https://user-images.githubusercontent.com/98563830/215885515-33c17df2-822f-42b6-b80b-7a7a5d5eb37f.png)

## Core concepts
<p><strong>The Colony</strong>. This is where the game takes place. The colony consists of
several <code>Place</code>s that are chained together to form a tunnel where bees can
travel through. The colony also has some quantity of food which can be expended
in order to place an ant in a tunnel.</p>

<p><strong>Places</strong>. A place links to another place to form a tunnel. The player can
put a single ant into each place. However, there can be many bees in a single
place.</p>

<p><strong>The Hive</strong>. This is the place where bees originate. Bees exit the beehive to
enter the ant colony.</p>

<p><strong>Ants</strong>. Players place an ant into the colony by selecting from the
available ant types at the top of the screen.
Each type of ant takes a different action and requires a different
amount of colony food to place. The two most basic ant types are the <code>HarvesterAnt</code>,
which adds one food to the colony during each turn, and the <code>ThrowerAnt</code>, which
throws a leaf at a bee each turn. You will be implementing many more!</p>

<p><strong>Bees</strong>. In this game, bees are the antagonistic forces that the player must
defend the ant colony from. Each turn, a bee either advances to the next place in
the tunnel if no ant is in its way, or it stings the ant in its way. Bees win
when at least one bee reaches the end of a tunnel.</p>

## Game Layout
Below is a visualization of a GameState
![colony-drawing](https://user-images.githubusercontent.com/98563830/215889158-a5ffedd2-2ac8-45ae-aee4-5f5ed61f700a.png)

## Objective Map
[ants_diagram.pdf](https://github.com/ddoanh/Ants-Project/files/10551301/ants_diagram.pdf)

