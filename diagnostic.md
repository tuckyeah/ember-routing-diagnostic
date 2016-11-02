# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
Inside the Ember Application Router, that's where we define our URL paths and locations. Inside the Ember Route, that's where we put our model hooks and where we retrieve data from the model to send to the template.
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    ember g route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    {{#link-to 'campus.boston'}}Boston{{/link-to}}
    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
    The second one defines a route for 'product', that is accessed by the URL
    path '/products/:product_id'.

    The first one creates a nested route, that will be a child of the products route,
    meaning that the full path for a product url will just be the '/:product_id', where :product_id is whatever id we put into it. They will likely both look the same in the URL
    bar, but must be accessed directly in different ways.
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    We'll use the variable 'params' to reference the value inside the route.
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    Initially, we have to reference data provided by a Route using the keyword
    'model' in our templates.
    ```
