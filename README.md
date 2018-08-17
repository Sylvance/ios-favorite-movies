# ios-favorite-movies
A sample application to find and save a list of your favorite movies. Created for use in the Pluralsight course [iOS and Swift from Scratch](https://app.pluralsight.com/library/courses/play-by-play-ios-swift-from-scratch/table-of-contents)

***Update 09/29/2017***: API requests to [The Open Movie Database](https://omdbapi.com) require an API key or they will be denied with a 401 response. In order to help keep this demo application running it is now leveraging the same API key as found in the [examples section of the site](https://omdbapi.com/#examples). If you abuse this demo key it will be banned so please use it only for demo/testing purposes.

## Prerequisites
1. MacOS (10.11.x or above)
2. Xcode 8.1

## Quick Start
1. Clone the repo and go to that directory
    ```bash
    git clone https://github.com/clarkio/ios-favorite-movies.git
    cd ios-favorite-movies
    ```

2. Open the project in Xcode
    ```bash
    open Favorite\ Movies/Favorite\ Movies.xcodeproj/
    ```
3. Select iPhone 7 for the simulator
4. Run the project by pressing CMD + R or clicking the Play button

## Main View
This view shows the list of the favorite movies. It uses a table view with a custom cell to show the favorite movies on the screen. The custom cell provides an ImageView to show the movie poster, a label for the movie title and a label for the year the movie was released. Lastly, it shows a "Find Movies" button which navigates to the Search View

## Search View
This view provides a way to search for movies to add to the favorites list. It uses a text field, button and table view with a custom cell to provide the search results. The custom cell is slightly different from the main view as it includes a "Fav" button that handles adding that movie to the main favorites list.

## Detail View
This view wasn't covered in the video, but is an example of performing an action when a table cell is selected. Within the main view's table view each table cell is selectable. When the cell is selected this triggers navigation to the Detail View. The Detail View shows the movie title along with the plot which is retrieved from the OMDb API.
