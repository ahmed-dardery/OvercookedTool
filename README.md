# OvercookedTool

A tool to convert Overcooked 2 saves between users/versions of the game.

## Requirements

Requires .NET Framework

## Usage

For each save game file (`*.save`) you wish to convert, decrypt using the existing user ID and then encrypt using the new user ID.

The user IDs are the long numbers in the name of the directory where the save files are saved. For example, for Steam on Windows we have `C:\Users\username\AppData\LocalLow\Team17\Overcooked2\<STEAM_ID>\*.save`, and for GOG Galaxy on Windows we have `C:\Users\username\AppData\LocalLow\Team17\Overcooked2\Saves\<GALAXY_ID>\*.save`

For example, to convert the Meta save file (which saves settings and cooks and various other metagame stuff):
```
.\OvercookedTool.exe decrypt C:\Users\Foo\AppData\LocalLow\Team17\Overcooked2\12345678912345679\Meta_SaveFile.save C:\Temp\Meta_SaveFile.json 12345678912345679
.\OvercookedTool.exe encrypt C:\Temp\Meta_SaveFile.json C:\Users\Foo\AppData\LocalLow\Team17\Overcooked2\Saves\987654321987654321\Meta_SaveFile.save 987654321987654321
```

## License

This code belongs to Team17 and I take no credit or responsibility over it.

