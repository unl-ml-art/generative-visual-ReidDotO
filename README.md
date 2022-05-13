# Project 3 Generative Visual

Reid Brockmeier, rbrockmeier2@unl.edu

## Abstract

For this project, I want to use a GAN to generate pokemon, and use the generated images to create a custom ROM Hack of Pokemon with those as the sprites. Ideally, I would like to replace every Pokemon in one game, but I am not sure if that is possible within the time restraints. As far as the method for generating, I am not entirely sure, but I believe there is a way to train/refine a GAN on your own images. If it is possible, I would like to use all the Pokemon to train it on. If not, I am sure that style transfer could work as well. An alternative project could be generating thumbnails for YouTube, but I do not think that would be all that interesting.

## Model/Data

- Pokemon Data
  - [Training Data](https://github.com/unl-ml-art/generative-visual-ReidDotO/blob/master/Pokemon%20Data/pokemon%20(1).txt) (data of all existing Pokemon)

## Code

- Pokemon Data Generation
  - [GPT-2 Notebook](https://github.com/unl-ml-art/generative-visual-ReidDotO/blob/master/Pokemon%20Data/gpt2-generate-finetune.ipynb)
- Pokemon Sprites Generation
  - [Collab Notebook from Max Woolf](https://colab.research.google.com/drive/1A3t2gQofQGeXo5z1BAr1zqYaqVg3czKd?usp=sharing)

## Results

GAME IS NOT INCLUDED HERE. If you want to play the game, see Technical Notes below.

- [Generated Pokemon Sprites](https://drive.google.com/drive/folders/1j32kMClGtk_8aHEY-FDXFY4Y1dxdqFOg?usp=sharing)

![00342](https://user-images.githubusercontent.com/83422507/168212248-604d1cf5-93f0-459d-a2b7-44252061a7b1.png)
![00564](https://user-images.githubusercontent.com/83422507/168212266-6484e0df-f25f-4bfb-9b75-bfe35ace6101.png)
![00778](https://user-images.githubusercontent.com/83422507/168212496-5da62ffd-aaeb-4c47-9673-e7c9169e9c10.png)

- Generated Pokemon Data
  - [1](https://github.com/unl-ml-art/generative-visual-ReidDotO/blob/master/Pokemon%20Data/generated_pokemon%20(1).txt), [2](https://github.com/unl-ml-art/generative-visual-ReidDotO/blob/master/Pokemon%20Data/generated_pokemon2%20(1).txt), [3](https://github.com/unl-ml-art/generative-visual-ReidDotO/blob/master/Pokemon%20Data/generated_pokemon3%20(1).txt), [4](https://github.com/unl-ml-art/generative-visual-ReidDotO/blob/master/Pokemon%20Data/generated_pokemon4%20(1).txt), [5](https://github.com/unl-ml-art/generative-visual-ReidDotO/blob/master/Pokemon%20Data/generated_pokemon5%20(1).txt), [6](https://github.com/unl-ml-art/generative-visual-ReidDotO/blob/master/Pokemon%20Data/generated_pokemon6%20(1).txt)

- In-Game Images
![Screenshot 2022-05-12 234927](https://user-images.githubusercontent.com/83422507/168213356-875a961e-f030-41df-a4ea-57775ff55a8b.png)
![Screenshot 2022-05-12 235541](https://user-images.githubusercontent.com/83422507/168213835-5f056db3-cda6-4f82-aaf2-1ee305bea87c.png)


- Video Documentation to come

## Technical Notes

TO PLAY THIS ROM YOU MUST RECREATE IT:
1. Obtain a ROM of Pokemon FireRed (no I will not explain how to do this)
2. Download [Pokemon Game Editor](https://github.com/Gamer2020/PokemonGameEditor/releases)
3. Launch PGE and open your ROM
4. Select "Pokemon Editor"
5. Import All Pokemon- use [Game Files.zip - Pokemon](https://github.com/unl-ml-art/generative-visual-ReidDotO/blob/master/Game%20Files.zip)
6. Import All Sprite Sheets- use [Game Files.zip - Sprites](https://github.com/unl-ml-art/generative-visual-ReidDotO/blob/master/Game%20Files.zip)
7. Play on an Emulator of your choice

TO MAKE YOUR OWN POKEMON (this takes way too long, so I do not suggest doing it):
1. Generate Pokemon sprites using [Collab Notebook from Max Woolf](https://colab.research.google.com/drive/1A3t2gQofQGeXo5z1BAr1zqYaqVg3czKd?usp=sharing)
2. Generate Pokemon data using [GPT-2 Notebook](https://github.com/unl-ml-art/generative-visual-ReidDotO/blob/master/Pokemon%20Data/gpt2-generate-finetune.ipynb)
3. Use [Pokemon Game Editor](https://github.com/Gamer2020/PokemonGameEditor/releases) to manually enter names, stats and other Pokemon data
4. Using your generated Pokemon sprites, you must do some work in photoshop to index them and use the correct format.
   1. Export the first sprite sheet and use this as a template.
   2. Cut your generated pokemon out of the background and place them in the spots of the existing Pokemon.
   3. Take some liberties for the back sprites as they are not generated.
   4. Make a background layer that is a color that does not appear in the sprite itself.
   5. Go to Image, Mode, and select Indexed Color.
   6. Change the colors to a custom profile and use 16 or less colors.
   7. Make sure that the first indexed color is your background color.
   8. Save as a png with the smallest file size.
   9. Import A-series Sprite sheet in PGE.



## References

- [Sprite replacing](https://www.pokecommunity.com/showthread.php?t=208837) (I did not use this because it was far more difficule, but it did help with indexing the images)
- [Max Woolf's Pokemon Generation](https://github.com/minimaxir/ai-generated-pokemon-rudalle)
