# Disclaimer

The contents of this repository are provided **for informational and research
purposes only**. They are **not financial, investment, or trading advice**, and
nothing here should be construed as a recommendation to buy, sell, or hold any
trading card, collectible, or other asset.

## What this is

- A measured index that estimates how much a Magic: The Gathering card's price
  swings right now, built from its public secondary-market price history: the
  annualized realized volatility of its weekly returns, its worst peak-to-trough
  drawdown, its swing range, and its jump and fat-tail behaviour.
- The model produces a relative score from 0 to 100, plus expected price-range
  bands at 3, 6, and 12 months. These are statistical estimates, not guarantees.
  A high score means the card has recently moved like other cards that were
  volatile; it does not predict the direction of the next move.

## What this is not

- It is **not** a forecast of which way a card's price will go.
- It is **not** a measure of what a card is worth.
- It is **not** an options-implied or model-implied volatility; it is a realized
  (historical) volatility used as a forward estimate.
- It is **not** a substitute for your own judgment or for professional advice,
  and it does **not** account for your individual financial situation, collection,
  tax position, or risk tolerance.

## Honest limitations

- This is version 1, a measured realized-volatility index. The only forward
  assumption is that volatility persists, which is real but moderate and
  mean-reverting, so the forward range bands are estimates, not promises.
- Cheap cards carry residual noise. Weekly sampling removes most price-
  discretization noise, but a sub-$2 card still shows more percentage wiggle than
  its small dollar moves justify. Imagery and examples are restricted to cards
  over $3 for this reason.
- Volatility is computed from one representative printing per card. Other
  printings (foils, old borders, collectible editions) can be far more or less
  volatile than the tracked copy.
- A stale price looks stable. A card no one trades shows little volatility
  because nothing reprices, not because it is genuinely calm. Such cards are
  flagged `stale_price` and should be read alongside the liquidity signal.

## No warranty

Outputs in this repository are provided "as is", without warranty of any
kind, express or implied, including but not limited to warranties of
merchantability, fitness for a particular purpose, accuracy, or
non-infringement. **The authors accept no liability** for losses, missed
gains, or any other damages arising from use of this material.

Cards and game terminology are property of Wizards of the Coast LLC. This
project is not affiliated with, endorsed by, or sponsored by Wizards of the
Coast.

By Cameraderie Cards.
