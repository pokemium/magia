# Magia

[![Go Report Card](https://goreportcard.com/badge/github.com/pokemium/magia)](https://goreportcard.com/report/github.com/pokemium/magia)
[![GitHub stars](https://img.shields.io/github/stars/pokemium/magia)](https://github.com/pokemium/magia/stargazers)
[![GitHub license](https://img.shields.io/github/license/pokemium/magia)](https://github.com/pokemium/magia/blob/main/LICENSE)

Magia is GBA emulator written in golang.

**Warning: This emulator is WIP, so many ROMs don't work correctly now.**

<img src="img/exe6g.png" width="320" alt="exe6g" />&nbsp;<img src="img/firered.png" width="320" alt="firered" />

<img src="img/mother12.png" width="320" alt="mother12" />&nbsp;<img src="img/dqm.png" width="320" alt="dqm" />

## Run

Please download latest binary from [Release](https://github.com/pokemium/magia/releases).

```sh
$ magia XXXX.gba
```

## Build

```sh
# go1.16.x
$ make build
$ ./build/darwin-amd64/magia XXXX.gba
```

## Key

| keyboard             | game pad      |
| -------------------- | ------------- |
| <kbd>&larr;</kbd>    | &larr; button |
| <kbd>&uarr;</kbd>    | &uarr; button |
| <kbd>&darr;</kbd>    | &darr; button |
| <kbd>&rarr;</kbd>    | &rarr; button |
| <kbd>X</kbd>         | A button      |
| <kbd>Z</kbd>         | B button      |
| <kbd>S</kbd>         | R button      |
| <kbd>A</kbd>         | L button      |
| <kbd>Enter</kbd>     | Start button  |
| <kbd>Backspace</kbd> | Select button |

## ToDo

- [ ] Window
- [ ] Mosaic
- [ ] Blend
- [ ] GUI
- [ ] Serial communication
- [ ] BG mode5
- [ ] GameBoy Compatibility
- [ ] Debug feature
- [ ] Fix some bugs

## Game Compatibility List

| Game Title             | Compatibility      |
| -------------------- | ------------- |
| バトルネットワーク ロックマンエグゼ3 BLACK | ✅ |
| ロックマンエグゼ4 トーナメント ブルームーン | ✅ |
| ロックマンエグゼ6 電脳獣グレイガ・電脳獣ファルザー | ✅ |
| ドラゴンクエストモンスターズ キャラバンハート | ✅ |
| MOTHER1+2 | ✅ |
| ポケットモンスター ファイアレッド | ✅ |


## Accuracy

| Test             | Result      |
| -- | -- | 
| [gba-tests/arm](https://github.com/jsmolka/gba-tests/tree/a6447c5404c8fc2898ddc51f438271f832083b7e/arm) | 408 |
| [gba-tests/thumb](https://github.com/jsmolka/gba-tests/tree/a6447c5404c8fc2898ddc51f438271f832083b7e/thumb) | 211 |
| [Memory tests](https://github.com/mgba-emu/suite/blob/04ada216ee13c56d786e54636ac980a71d791145/src/memory.c) | 1100/1552 |
| [I/O read tests](https://github.com/mgba-emu/suite/blob/04ada216ee13c56d786e54636ac980a71d791145/src/io-read.c) | 12/123 |
| [Shifter tests](https://github.com/mgba-emu/suite/blob/04ada216ee13c56d786e54636ac980a71d791145/src/shifter.c) | 140/140 |
| [Multiply long tests](https://github.com/mgba-emu/suite/blob/04ada216ee13c56d786e54636ac980a71d791145/src/multiply-long.c) | 52/72 |
| [BIOS math tests](https://github.com/mgba-emu/suite/blob/04ada216ee13c56d786e54636ac980a71d791145/src/bios-math.c) | 530/625 |
| [DMA tests](https://github.com/mgba-emu/suite/blob/04ada216ee13c56d786e54636ac980a71d791145/src/dma.c) | 964/1256 |
| [Misc. edge case tests](https://github.com/mgba-emu/suite/blob/04ada216ee13c56d786e54636ac980a71d791145/src/misc-edge.c) | 6/10 |

## References

- [GBATEK](https://problemkaputt.de/gbatek.htm)
- [gba_doc_ja](https://github.com/pokemium/gba_doc_ja)
- [gdkchan/gdkGBA](https://github.com/gdkchan/gdkGBA)
