Key Components :                                                                                                                                                      
  1-Global Variables :- 
     - products: A jQuery selector for the product display area.
     - loadingScreen: A jQuery selector for the loading screen element.
     - searchInput: A jQuery selector for the search input field.
     
  2-Functions :-
    - showScreen(): Displays the loading screen and hides the body overflow (scroll bar).
    - hideScreen(callback): Hides the loading screen after a fade-out effect and restores body overflow. It also executes an optional callback function after hiding.
    - getAllProducts(): Fetches all products from the API, shows the loading screen, and calls displayProducts() to update the UI. It handles errors gracefully.
    - getCategoryProducts(value): Fetches products based on the selected category. Triggered by user input in the search bar.
    - displayProducts(arr): Accepts an array of products and dynamically generates HTML to display each product in the grid layout.
    
Approach :                                                                                                                                
  1-Loading Screen Management
    The application utilizes a loading screen to indicate data fetching. The showScreen() function makes the loading screen visible, while hideScreen() hides it after the data is fetched.                                                                                    
                                             
  2-Data Fetching
    - Asynchronous functions (async/await) are used to fetch product data from the Fake Store API.
    - The getAllProducts() function retrieves all products initially, while the getCategoryProducts(value) function filters products based on user input.                                                                                                                      
                  
  3-User Interaction 
    - The application listens for keyup events on the search input. As the user types, the getCategoryProducts() function is called to fetch and display products that match the entered -category.
  4-Dynamic Display of Products
    - The displayProducts(arr) function generates and inserts HTML for each product into the DOM, utilizing a Bootstrap grid layout for responsiveness. Each product displays its image, title, price, and rating.
