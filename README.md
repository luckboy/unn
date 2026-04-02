# UNN

Micro neural network library that is written in the Unlab scripting language. This library implements
basic neural networks that can be trained by training functions of this library. Also, this library
contains optimization algorithms which can be used to train neural network.

## Installation

You can install this library by invoke the following command:

```
unlab-pkg install github.com/luckboy/unn
```

## Usage

You can use this library in add the following lines in the `Unlab.toml` file:

```toml
[dependencies]
"github.com/luckboy/unn" = "0.1.0"
```

Then you install this library as dependency for your project invoke the following command:

```
unlab-pkg install-deps
```

Then you add the following line in the `lib.un` file:

```
uselib("pl.luckboy/unn")
```

## Example

The following example presents the training of neural network:

```
uselib("pl.luckboy/unn")
usemods("pl_luckboy_unn")
usevars("pl_luckboy_unn")
net = mlp(.[ 10, 100, 15 .], .[ tanh .], se, xavier_init)
X = [rand() fill 100; fill 10]
Y = [rand() fill 100; fill 15]
net2 = etrain(100, net, X, Y, { eta: 0.1 }, alg::gd, none, true, true)?
```

## License

This library is licensed under the Mozilla Public License v2.0. See the LICENSE file for the full
licensing terms.
