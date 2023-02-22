# pokemon-analysis
## Overview

Analysis carried out in this repository uses data from the
[Pokemon dataset](https://www.kaggle.com/datasets/abcsds/pokemon).
For instructions on how to obtain these data see the **Setup** section.
Also, this analysis are reproducible and all needed is documented here.

Description from Kaggle:

"
*This data set includes 721 Pokemon, including their number, name, first
 and second type, and basic stats: HP, Attack, Defense, Special Attack,
 Special Defense, and Speed. It has been of great use when teaching
 statistics to kids. With certain types you can also give a geeky
 introduction to machine learning. The data as described by Myles
 O'Neill is:*"

- #: ID for each pokemon
- Name: Name of each pokemon
- Type 1: Each pokemon has a type, this determines weakness/resistance to attacks
- Type 2: Some pokemon are dual type and have 2
- Type 2: Some pokemon are dual type and have 2
- Total: Sum of all stats that come after this, a general guide to how strong a pokemon is
- Total: Sum of all stats that come after this, a general guide to how strong a pokemon is
- HP: Hit points, or health, defines how much damage a pokemon can withstand before fainting
- HP: Hit points, or health, defines how much damage a pokemon can withstand before fainting
- Attack: Base modifier for normal attacks (eg. Scratch, Punch)
- Defense: Base damage resistance against normal attacks
- SP Atk: Special attack, the base modifier for special attacks (e.g. fire blast, bubble beam)
- SP Def: Base damage resistance against special attacks
- Speed: Determines which pokemon attacks first each round

## Setup

Kaggle API was used to get data. If it's your first time using it,
follow the steps "Installation" and "API credentials" in this
[link](https://github.com/Kaggle/kaggle-api).

Download the data using:

`kaggle datasets download -d abcsds/pokemon -p data/`

Unzip it with the command:

`tar .\data\pokemon.zip -C data/`

Data compression efficiency and encoding are better with
[Parquet](https://parquet.apache.org/) formatting, so we transform or data:

`python .\scripts\to_parquet.py`

You are ready!

## Structure

## Credits

Guilherme Urbano (@guidurbano)

## License

MIT License

Copyright (c) 2023 Guilherme Urbano

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
