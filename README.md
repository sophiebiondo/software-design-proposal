# software-design-proposal

<hs6> The client, The Gaming Room, commissioned a web-based multiplayer game called Draw It or Lose It. They needed a system where multiple teams (each with   multiple players) compete over four timed rounds by guessing stock‐drawing “clues.” Key software requirements were:
- Support one or more teams per game
- Allow multiple players per team
- Enforce unique game and team names
- Guarantee only one active game instance in memory via unique identifier


I translated the client’s needs into a clear design document starting from executive summary, through requirements, to domain model and recommendations. Each section tied directly back to a specific client request. The domain model reflected real‐world relationships (Game, Teams, Players) and used OOP best practices (inheritance, encapsulation, singleton) to meet requirements efficiently. 


Working through the design document helped me to think holistically before coding. Defining constraints and dependencies early (e.x. unique IDs, single‐instance enforcement, distributed communications) guided my infrastructural choices and prevented midstream rewrites. Having a solid requirements-to‐design mapping made it straightforward to scale the codebase around clear patterns.



Further down the line, I’d expand the Design Constraints section to include an Observer/Publish–Subscribe pattern for real‐time updates (e.x. broadcasting new drawing frames to clients). Documenting that pattern and its event flows would sharpen the architecture around live rendering and guess‐submission events, improving clarity for developers.


I mapped teams, players, unique naming, and singleton behavior to core classes and services. The design supported real user flows (joining a game, guessing within time limits, fallback guessing). Keeping user needs at the forefront prevents wasted effort and delivers a solution that actually works in deployment.


Here's a list of my primary software design strategies:
- Requirements analysis (business vs. technical)
- Domain modeling (UML classes reflecting key entities)
- Design‐pattern selection (singleton for single‐instance, composition for team/player aggregation)
- Infrastructure mapping (Linux‐based hosting, REST/WebSocket communications)
  </hs6>

