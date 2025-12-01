> [!CAUTION] 
> This repository is still being developed and the current code is not functional.

# serato-sessions
serato-session is a Python library for reading Serato DJ sessions. It is able to do this by either reading a file from .session files or Serato Playlists. Reading session info will let you see the current playing song and previously song history.

## Installation
This library is still under development and is not yet available for installation. We hope to have it available soon on pip. Please check back later for updates.

## Usage
Here are some basic examples of how to use this library.

**Get currently playing song and history from session files**
```python
from serato_sessions import Sessions

sessions = Sessions()

session = Sessions.get_latest_session
print(f'Currently playing: {session.now_playing.title} by {session.now_playing.artist} \n')
print('Previously played:')
for track in session.history:
    print(f'{track.start_time} - {track.title} by {track.artist}')
```

<br>

**Get currently playing song and history from a Serato playlist**
```python
from serato_sessions import Playlist

playlist = Playlist('https://serato.com/playlists/<username>/<playlist_name>')

print(f'Currently playing: {playlist.now_playing.title} by {playlist.now_playing.artist} \n')
print('Previously played:')
for track in playlist.history:
    print(f'{track.start_time} - {track.title} by {track.artist}')
```

## Documentation
Check out the [Wiki](https://github.com/tscharich/serato-sessions/wiki) for full documentation.

## Contributing
At this time, I ask that you do not send any pull requests. I do hope to hope to open this up for contributions in the future.

## Problems?
If the library isn't working, please [open an issue](https://github.com/tscharich/serato-sessions/issues/new) on this GitHub repository. If there is a security issue please [report it directly](https://github.com/tscharich/serato-sessions/security/advisories/new).

## Questions?
If you have any questions, please feel free to make a post in our [GitHub Discussions](https://github.com/tscharich/serato-sessions/discussions)

## Using this software in your own projects?
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Special Thanks
### Ely Miranda ([e1miran](https://github.com/e1miran))
Creator of Now-Playing-Serato, which this repository is a fork of.
<br>
[![e1miran/Now-Playing-Serato](https://img.shields.io/badge/github-e1miran%2FNow--Playing--Serato-blue?logo=github&label=github)](https://github.com/e1miran/Now-Playing-Serato)
