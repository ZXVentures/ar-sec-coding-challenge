# Back-end Challenge

## About the Challenge 

There are many factors to consider when picking your next beer. One of the most important ones is _bitterness_. The International Bitternes Unit (IBU) is the unit used to measure the bitterness of a beer.

![Beers](beers.jpeg)

We would love to be able to recommend our customers what is the best combination of beers for them. 

How do we do it? We ask our customers what's the exact level of bitterness they are looking for and we will suggest them two different beers that together sum up to that number. 

For example, if we have the following beers. 

| Brand             | IBU   |
|-------------------|-------|
| Patagonia         | 36    |
| Quilmes Stout     | 36    |
| Quilmes Cristal   | 15    |
| Stella Artois     | 24    |

And our customer ask for a total IBU of 39, our system could answer Quilmes Cristal and Stella Artois because 15 + 24 = 39. 

### Considerations 

- In case no valid sum is found, the recommender should return an empty array
- The function gets a list of IBUS (integer values greater than 0) and a target value
- It must return one solution only (there may be more than one)
- The signature of the method should be:  
	`findTwoBeers(beers: number[], target: number) : number[]`
- The return value must be an array with two items (in case a solution exists), or an empty array in case no answer exists. Return values should be the index of the input array.

Examples:

```
# Valid output
Input: [10, 15, 20]
Target: 30
Output: [0, 2]

# No valid output
Input: [10, 15, 20]
Target: 40
Output: []
```

### What should you build?

1. Create a function that solves the problem
2. Use AWS Lambda and API Gateway to create a REST endpoint that enables calling the function like this: 
    ```
    POST /findTwoBeers
    {
      beers: [15, 20, 25, 39, 12, 18, 19, 21], 
      target: 35
    }
    ```
    The output must match the following format: 
    ```
    status: 200
    response body (application/json)
    {
      index: [0, 1]
    }
    ```
3. Add tests with coverage > 70%
4. Use the README file to explain what is the time and space complexity of your solution. Please don't forget to include instructions on how to run the code. 
5. Extra: if you want to publish your solution in your own AWS account you can share a link to API Gateway, so we can test it. 

## How to submit
Create a public repo in github and send an email to matias@siempreencasa.com.ar with a link to it. 
