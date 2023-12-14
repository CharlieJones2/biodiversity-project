# Analysing Biodiversity in National Parks in the USA

This project analyses biodiversity data across national parks in the USA, with the aim of answering the following questions:

- How many endangered species are present in these national parks?
- Are certain types of species (mammal, reptile, amphibian etc) more likely to be endangered than others?
- Is there any significant difference in the probability of one species being endangered relative to another?

Using Pandas, I load the data, manipulate the datasets and perform some exploratory data analysis to get a feel for the type of data we are working with.
After this, I delve deeper into the questions.

---

### Analysis

In answering the first question, I create a DataFrame containing only endangered species, and perform a `groupby()` using the species column in order to see how many of each species are endangered.
I visualise these results using the `sns.countplot()` method, the results of which are as follows:

![Countplot](https://github.com/CharlieJones2/biodiversity-project/blob/main/endangered.png)

#

To answer the second question, I find the proportion of each species that are endangered, and identify the percentage of each species that are endangered.
Mammals are found to be the most likely species to be endangered, with 3.27% of mammals in the dataset being classed as endangered.

#

In order to test whether the difference in the probability of each species being endangered is significant, I perform chi-squared tests between each pair of species.
Using the obtained p-values, I am able to see for which species the difference in probability is significant.
By reporting only p-values less than 0.05, I find that the difference in endangered status rates between vascular plants and all other species is significant, which could be expected seeing as the proportion of endangered vascular plants is much lower than all other categories.
Moreover, there is a significant difference between mammals and birds, the groups with the highest and second lowest proportion of endangered species respectively.

---

# Conclusions

### How many species in the dataset are endangered?

- **There are 16 endangered species in the dataset**, comprising of 7 mammals, 4 birds, 3 fish, 1 amphibian and 1 vascular plant.
- There were no reptiles or non-vascular plants which are endangered in the dataset.

### Are certain types of species more likely to be endangered than others?

- This question was answered by comparing the proportion of species belonging to each category which were endangered.
- The analysis found that **mammals were the most likely to be endangered**, with 3.27% being endangered, followed by fish, amphibians, birds and vascular plants.

### Is there any significant difference in the probability of one species being endangered relative to another?

- This question sought to determine whether the difference in probability of one category being endangered was significantly different among categories.
- For categories where the difference is found to be significant, it can be concluded that the chance of a species belonging to this category being endangered is different to the chance of a species belonging to another category being endangered.
- The analysis showed that **the probability of vascular plants being endangered was significantly lower than the probability of mammals, fish, amphibians and birds.**
- It also found **the probability of mammals being endangered was significantly different to the probability of birds being endangered.**
