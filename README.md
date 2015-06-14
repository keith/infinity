# Infinity

My infinity keyboard configuration.

## Setup

Install dependencies:

```
brew tap Homebrew/brewdler && brew bundle
```


## Steps to update

Either:

1. Update the `*.kll` files on your own

OR

1. Go to [the configurator](http://configurator.input.club/) make some
   changes and download the results
1. Update `base-0.kll` with changes to the main layout and update
   `functions-1.kll` with changes to the first layer. (In theory other
   layers could be added with slight modifications as well).
1. Clone the [controller](https://github.com/kiibohd/controller) and the
   [KLL compiler](https://github.com/kiibohd/kll) (inside the controller
   directory).
1. Copy `*.kll` from here to `controller/kll/layouts/` (`cp *.kll
   ../controller/kll/layouts`)
1. In the controller directory apply `controller.patch` (`git apply
   ../infinity/controller.patch`)
1. `cd Keyboards && ./infinity.bash`
1. This should succeed and create a `template` directory in the current
   directory.
1. Connect the keyboard to your machine and press the button on the
   bottom, make sure the orange light turns on.
1. `cd template && ./load`
1. Copy the generated `kiibohd.dfu.bin` and updated layout files to this
   repository and check it in.

## Steps to reflash without changes

1. Connect the keyboard to your machine and press the button on the
   bottom, make sure the orange light turns on.
2. `dfu-util -D kiibohd.dfu.bin`


### Resources

- <https://www.massdrop.com/keyboard/infinity/assembly>
- <https://github.com/cubiq/KiiConf/blob/master/build_layout.bash>
- <https://github.com/kiibohd/controller/wiki>
- <http://configurator.input.club/>
