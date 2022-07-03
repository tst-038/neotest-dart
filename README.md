# neotest-dart

This plugin provides a [Dart](https://dart.dev/) and [Flutter](https://flutter.dev/) tests adapter for the [Neotest](https://github.com/rcarriga/neotest) framework.

## Status:

**Work in progress 🚧**.

## Installation

Using packer:

```lua
use({
  'nvim-neotest/neotest',
  requires = {
    ...,
    'sidlatau/neotest-dart',
  }
  config = function()
    require('neotest').setup({
      ...,
      adapters = {
        require('neotest-dart') {
             command = 'flutter', -- Command being used to run tests. Defaults to `flutter`
                                  -- Change it to `fvm flutter` if using FVM
                                  -- change it to `dart` for Dart only tests
          },
      }
    })
  end
})
```

## Usage

_NOTE_: all usages of `require('neotest').run.run` can be mapped to a command in your config (this is not included and should be done by the user)

#### Test single function

To test a single test hover over the test and run `require('neotest').run.run()`

#### Test file

To test a file run `require('neotest').run.run(vim.fn.expand('%'))`

## Contributing

This project is maintained by the nvim Dart/Flutter community. Please raise a PR if you are interested in adding new functionality or fixing any bugs
If you are unsure of how this plugin works please read the [Writing adapters](https://github.com/nvim-neotest/neotest#writing-adapters) section of the Neotest README. When submitting a bug, please include an example spec that can be tested.
