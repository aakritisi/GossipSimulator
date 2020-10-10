# Gossip Protocal Simulation

Gossip Algorithm for information propagation:The Gossip algorithminvolves the following:•Starting: A participant(actor) it told/sent a rumor(fact) by the mainprocess•Step: Each actor selects a random neighbor and tells it the rumor•Termination: Each actor keeps track of rumors and how many times ithas heard the rumor. It stops transmitting once it has heard the rumor10 times (10 is arbitrary, you can play with other numbers or other stoppingcriteria).
Push-Sum algorithm for sum computation:•State: Each actor Aimaintains two quantities: s and w. Initially, s =xi= i (that is actor number i has value i, play with other distribution ifyou so desire) and w = 1.•Starting: Ask one of the actors to start from the main process.•Receive: Messages  sent  and  received  are  pairs  of  the  form  (s, w).  Uponreceive, an actor should add received pair to its own corresponding values. Upon receive, each actor selects a random neighbor and sends it amessage.•Send: When sending a message to another actor, half of s and w is keptby the sending actor and half is placed in the message.•Sum estimate: At any given moment of time, the sum estimate is s/wwhere s and w are the current values of an actor.•Termination: If  an  actorratio s/w did  not  change  more  than  10-10in3 consecutive  rounds  the  actor  terminates. WARNING:  the  values sand w independently never converge, only the ratio does.Topologies:The  actual  network  topology  plays  a  critical  role  in  the  dissemination speed  of  Gossip  protocols.  As  part  of  this  project  you  have  to  experimentwith various  topologies.  The  topology  determineswho  is  considered  a  neighborin  the above algorithms.•Full Network:Every actor is a neighbor of all other actors. That is,every actor can talk directly to any other actor.•Line:Actors are arranged in a line. Each actor has only 2 neighbors(one left and one right, unless you are thefirstor last actor).•Random  2D  Grid:Actors  are  randomly  position  at  x,y coordinateson  a  [0-1.0]x[0-1.0] square. Two actors are connected if they are within.1 distance to other actors.•3D torus Grid:Actors  form  a  3D  grid.  The  actors  can  only  talk  to  the  gridneighbors.And, the actorson outer surfaceareconnected to other actors on opposite side, such that degree of each actor is 6.


## Installation

If [available in Hex](https://hex.pm/docs/publish), the package can be installed
by adding `proj2` to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [
    {:proj2, "~> 0.1.0"}
  ]
end
```

Documentation can be generated with [ExDoc](https://github.com/elixir-lang/ex_doc)
and published on [HexDocs](https://hexdocs.pm). Once published, the docs can
be found at [https://hexdocs.pm/proj2](https://hexdocs.pm/proj2).

