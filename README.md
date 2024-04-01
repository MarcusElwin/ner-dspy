# ner-dspy
In this repo, you will find a small example of using [DSPy](https://dspy-docs.vercel.app/) for a *data extraction* / *Named Entity Recognition* (NER) Task. The task is to extract food-related entities from a *recipe*. One example recipe can be found in the `./data` folder.

This workflow illustrates how to use `DSPy` to extract entities by employing the following prompt engineering techniques:
* *Chain-of-Thought* (CoT)
* *Prompt-Chaining* (PC)
* *Function Calling* using `TypedPredictor` from `DSPy`

The output of running the program is a list of `FoodEntities`:
```python
{
  "entities": [
    {
      "food": "pork belly",
      "quantity": 2,
      "unit": "lb",
      "physical_quality": null,
      "color": ""
    },
    {
      "food": "green onions",
      "quantity": 2,
      "unit": "items",
      "physical_quality": "or 3 if small",
      "color": ""
    },
    ...
  ]
```

## Setup ⚙️
1. Make sure to install `poetry` on your system see e.g. instructions [here](https://python-poetry.org/docs/#installation)
2. Install requirements 
   ```sh
   poetry install --no-root
   ````
## Run notebook 📓
To run the `jupyter` server use:
```sh
poetry run jupyter lab
```

