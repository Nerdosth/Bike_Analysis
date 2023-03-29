
# MTB Bike Data Retrieval and Cleaning

This code retrieves mountain bike data from the 99Spokes API and cleans it for analysis. The goal of this repository is to demonstrate the use of technology and coding and how it drastically improves the time to do market research. With the help of the 99spokes web scraping site and the API they built, with access, I wrote a python script that can loop through the dataset and export it to a CSV file. From there, I can use powerful tools such as Tableau to create visuals and views that allow users to drill into the data.

![1680108276589](https://file+.vscode-resource.vscode-cdn.net/c%3A/Users/erdos/Class%20Folder/Bike_Analysis/image/README/1680108276589.png)![image](https://user-images.githubusercontent.com/76061893/205497445-ab39cf19-f7d8-4007-b82a-297b42adc626.png)

You can find the Dashboard here: https://public.tableau.com/app/profile/nicholas.erdos.thayer/viz/MountainBikeAnalysis/MountainBikeTrends

## Dependencies

This code requires the following dependencies:

* `api_key`: An authentication token for the 99Spokes API.
* `requests`: A library for making HTTP requests.
* `json`: A library for working with JSON data.
* `json_normalize`: A function for flattening JSON data into a pandas dataframe.
* `flatten`: A function for flattening nested dictionaries.
* `pandas`: A library for working with dataframes.
* `regex`: A library for working with regular expressions.

## How to Use

To use this code, first ensure that you have obtained an authentication token for the 99Spokes API. This token should be saved as a string in a file called `api_key.py`, like so:

```
Auth_Token = "your_api_key_here"
```

Next, set the search parameters for the bikes you wish to retrieve. You can adjust the following parameters:

See API documention for help: https://api.99spokes.com/docs

* `search`: A string query to filter bikes by name or description.
* `model_year`: A list of integers representing the model years to filter by.
* `cat`: A string representing the bike category to filter by (e.g. "mountain", "road", etc.).
* `sub_cat`: A list of strings representing the bike subcategories to filter by.
* `Brand`: A list of strings representing the bike brands to filter by.
* `eBike`: A string representing whether to include electric bikes ("true" or "false").
* `frameset`: A string representing whether to include framesets only ("true" or "false").
* `include`: A string representing the fields to include in the response.

Once you have set your search parameters, simply run the code in Jupyter Notebook. It will retrieve the data and output a cleaned dataframe called `mtb_df`, which will be saved as a CSV file named "MTB.csv".

## Limitations

This code is designed specifically for retrieving and cleaning mountain bike data from the 99Spokes API. It may not work for other types of bikes or other APIs. Additionally, the code may need to be modified if the API changes its structure or if new data cleaning requirements arise.
