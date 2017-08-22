# Replays

A replay lets you review what happened during a game. You can see the actions
and observations that each player made as they played.

Blizzard is releasing a large number of anonymized 1v1 replays played on the
ladder. You can find instructions for how to get the
[replay files](https://github.com/Blizzard/s2client-proto#downloads) on their
site. You can also review your own replays.

Replays can be played back to get the observations and actions made during that
game. The observations are rendered at the resolution you request, so may differ
from what the human actually saw. Similarly the actions specify a point, which
could reflect a different pixel on the human's screen, so may not have an exact
match in our observations, though they should be fairly similar.

Replays are version dependent, so a 3.15 replay will fail in a 3.16 binary.

You can visualize the replays with the full game, by putting SC2Replay file into [SC2Root]/Replays (e.g. C:\Program Files (x86)\StarCraft II\Replays), calling `pysc2.bin.replay_info` path/to/replay/file, and putting the corresponding SC2Map under [SC2Root]/Maps/location/suggested/by/replay/info (e.g. C:\Program Files (x86)\StartCraft II\Maps\mini_games\*.SC2Map).

Or, with `pysc2.bin.play` to replay under abstraction.

Alternatively you can run `pysc2.bin.replay_actions` to process many replays
in parallel.

