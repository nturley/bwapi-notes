Voronoi Analysis
---------------

Voronoi analysis simplifies reasoning about continuous spaces.

The most common usage of voronoi analysis is to place generators along
the edges of unpassable regions
so that units can follow the vertices to maintain the maximum clearance
from barriers. Minima in the clearance represent chokepoints. This also
simplifies path finding by turning the irregular shape of the map into
a graph.

Treating threats as generators allows you to do threat aware path planning. This allows you to
reason about optimal paths for running past enemy defenses. Edges represent gaps
in enemy defenses.

Treating units as generators also allows you to reason about unit formations.
Moving toward centroids spreads your units out to fill the available space.
Moving toward midpoints of enemy cell edges surrounds the enemy.

All of these analyses have different rules and assumptions as you build your
voronoi data structure. For instance when using units as generators if you
treat the cell as the area that the unit can reach in the smallest amount of
time, then it will lose accuracy if it doesn't take barriers into account.
Whereas, when considering flying units or ranged units, it may not be
as important.

