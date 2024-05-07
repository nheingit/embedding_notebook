# Setup

to install the dependencies here, you will need to run `poetry install`, if that doesn't work for you, you can also try `poetry install --no-root`

After that, intialize the shell: `poetry shell`

And then kick start the jupyter server by running `jupyter lab`

Then the only thing you should have to edit is adding your openai key to the notebook.

From there you can use the UI, and run all of the cells to get the data frame vizualizations.

The only edit you should have to make, is putting in your OpenAI API key.

Finally, I only embed the first 10 items in the array, as we won't be using this, so there's no point in spending $$ embedding ALL of the files.

## Overview

In this project I opted to do things a bit differently than we did in the offical project module. Just to see the data viz better and show you a more naive approach. This implementation adds the link to every single chunk. This means we're paying a bit extra as those are extra tokens. The better way to do this would be to handle the "citation" portion in the questions.py module, by having a seperate 'url' or 'filename' column that you could add into the context. This would be a cheaper, more consistent way, but I wanted to show you a different approach to the problem.

Often times you will build out something like this, and then migrate over to the more efficent implementation after proving out the concept.
