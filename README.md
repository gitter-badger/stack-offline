# stack-offline

Build [stack](http://docs.haskellstack.org) projects offline

## Design

### Utility `stack-offline`

Packs everything you need to develop without internet connection.
Packing itself does use internet connection.

Parameters:
- `--resolver` 
  - (mandatory) use specified snapshot
- `--minimal` 
  - pack only build tools, without testing, profiling and other tools
- `--system-ghc` 
  - do not pack GHC (default)
- `--no-system-ghc` 
  - do pack GHC

Output: 
- big `tgz` archive (from hundreds of megabytes in minimal case to several gigabytes and beyond) with packages and compiler.
- a script extracting everything into proper positions in user's `~/.stack`.
