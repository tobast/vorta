# Vorta - BorgBackup GUI

[Vorta](http://memory-alpha.wikia.com/wiki/Vorta) is a GUI for [BorgBackup](https://borgbackup.readthedocs.io). It's in alpha status and currently has the following features:

- Select and manage SSH keys
- Initialize new remote Borg repositories
- Create new Borg snapshots (backups) from local folders
- Display existing snapshots and repository details.
- Settings stored in sqlite
- Borg binary integrated

Planned features:

- Scheduling for background backups.
- Rule-based scheduling by time, Wifi SSID, etc.
- Repo pruning
- Repo checking
- Securely save repo password in Keychain instead of database.
- Handle encrypted SSH keys
- Check for duplicate source dirs

## Development
Conda is used for dependency management. Create a new virtual env using:
```
$ conda env create environment.yml
```

Qt Creator is used to edit views. Install using Homebrew and then open the .ui files in `vorta/UI`:
```
$ brew cask install qt-creater
$ brew install qt
```

To build a binary package:
```
$ pyinstaller --clean --noconfirm vorta.spec 
```

## Author
(C) 2018 Manuel Riel for [BorgBase.com](https://www.borgbase.com)

## License and Credits
- Licensed under GPLv3. See LICENSE.txt for details.
- Uses the excellent [BorgBackup](https://www.borgbackup.org)
- Based on PyQt and Qt.
