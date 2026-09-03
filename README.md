Part 1: Data Collection through Web Scraping

In this first part, I extracted the pokemon data from the pokedex. To do this, I first found the information I wanted.
Implemented a 4 second delay to avoid overloading the server, then began scraping the pokedex table!
I used requests to first fetch the webpage and BeautifulSoup to parse the HTML into the JSON format.
I then saved the scraped data into that JSON file.

Part 2: Data Loading and Preprocessing

To clean and structure the JSON dat for analysis by loading it into a Pandas DataFrame and performing necessary preprocessing steps to facilitate analysis.
First, I loaded the JSON data and converted it into a Pandas DataFrame using pd.DataFrame.from_dict.
I split types into two columns, primary and secondary. And abilities into primary and secondary.
Then, I extracted male and females % from the gender field and made two new columns for the two of them. Finally, I removed any redundant columns after splitting and saved it into a pickle file.

Part 3: Analysis of Pokémon Distribution by Primary Type

In this step, the aim was to sort the pokemon counts for each primary type using the value_counts method.#
To do that, I mapped each pokemon to a colour value for data visualation!
I used ploty to make myself a bar chart, sorted each type by colour and finally just added some titles and labels to help make the chart more clear and concise.
Doing this, I can now analyse which pokemon tpye is the most and least common.

<img width="1711" height="518" alt="image" src="https://github.com/user-attachments/assets/446282ff-e807-4e2c-80c1-699bb0bda020" />

Part 4: Comparative Analysis of Pokémon Distribution by Primary Type and Generation

This part was to explore how pokemon types are distributed across different generations.
Here, I organized the data by grouping the generation and primary_type. By doing so I also counted how many of each type within each generation using groupby and size.
As same as before, I would use plotly to make grouped bar charts for each type in the generation. Also using a similar colour scheme.
Though this time, I would use a stacked bar chart. Mostly just for visual purposes as it makes the comparison across generations much more clear.
By analsying these graphs, I can see dragons are much more prevalent in the newer generations!

<img width="1711" height="527" alt="image" src="https://github.com/user-attachments/assets/5eb44b6e-44d4-442e-aace-1a5f1eb381fc" />

Height and Weight

Here, I made a scatter plot to visualise height and weight relationships.
I used height_m and weight_kg columns for plotting.
Added hover tooltips to display all the names.
We can see in the chart most of the pokemons are clustered together, leaving some serious outliers on the graph for extremely heavy and tall pokemons.

<img width="1695" height="515" alt="image" src="https://github.com/user-attachments/assets/b1dacc43-6563-4912-b543-5f1434e35208" />

Stats

This step involved visualising the stats of the pokemon. Their total stats across the generations.
First, I summed up the stats (I had some problems in scraping however.) into a new column.
Put together a box plot using plotly and used colours for reference once again.

