# Leela Chess Zero Colab Notebooks

A collection of colab notebooks demonstrating how to perform various development, training, and testing tasks for leela chess zeo (lc0) in Google Colaboratory.

## Elo Testing

<a href="https://colab.research.google.com/github/chanind/lc0_elo_testing/blob/main/Lc0_Elo_Testing.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

This Colab implements the ideas from the [Lc0 Testing Guide](https://lczero.org/dev/wiki/testing-guide/) to test out Lc0 by having it compete against other chess engines. Edit this Colab to test out different configurations or networks for Lc0, or use it as as base for your own explorations. The implementation presented here just runs standard Lc0 against standard Stockfish.

## Rescoring

<a href="https://colab.research.google.com/github/chanind/lc0_colab_notebooks/blob/main/lc0_rescoring.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

This Colab demonstrates how to perform rescoring on the training data used by Lc0. Rescoring makes uses of [syzygy tablebases](https://syzygy-tables.info/), which are lists of perfect endgames for all games with less than 5 (or 6 or 7) pieces remaining on the board. If any training games end up in a position that's known in the tablebase, the rescorer will rewrite the game using the known perfect play from the tablebase so that leela can lean from a perfect endgame rather than the potential mistakes in the traning game.

Rescoring is used in the training of all the best nets for leela, and should always be used before running training for best results.
