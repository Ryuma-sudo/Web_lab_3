
# Task 2.2: GitHub Repository Finder

This report details the functions used in the GitHub Repository Finder application.

## Functions

### `searchRepositories(query, sort = 'stars', page = 1)`

This asynchronous function is responsible for fetching repository data from the GitHub API. It constructs a URL with the user's search query, selected sort option, and the current page number. It then uses the `fetch` API to make a GET request and returns the repository items from the JSON response.

### `displayRepositories(repos, append = false)`

This function takes an array of repository objects and displays them on the page. It dynamically creates HTML for each repository using the `createRepoCard` function and inserts it into the `repoList` element. It also handles the visibility of the "Load More" button based on the total number of results.

### `createRepoCard(repo)`

This function generates the HTML structure for a single repository card. It takes a repository object as input and returns an HTML string. This string includes the repository's name, description, and metadata like stars, forks, and language.

### `performSearch()`

This function is triggered when the user initiates a new search. It retrieves the search query and sort option from the input fields, resets the pagination, and clears any previous results or errors. It then calls `searchRepositories` to fetch the data and `displayRepositories` to show the results.

### `loadMore()`

This function is called when the user clicks the "Load More" button. It increments the current page number and fetches the next set of results using `searchRepositories`. The new results are then appended to the existing list by calling `displayRepositories` with the `append` parameter set to `true`.

### `showError(message)`

This function displays an error message to the user. It takes a message string and inserts it into the `errorMessage` element on the page, styled in a distinct error box.

### `clearError()`

This function simply clears any error messages that are currently being displayed. It sets the `innerHTML` of the `errorMessage` element to an empty string.

### `formatNumber(num)`

This utility function formats large numbers for better readability. It converts numbers over a million to a 'm' suffix and numbers over a thousand to a 'k' suffix, making the star and fork counts easier to parse at a glance.
