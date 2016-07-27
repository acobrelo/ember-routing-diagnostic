# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    The App Router mainly specifies the paths for each features so that Ember
    knows where to look for the files upon some action. The main tasks inside
    an Ember Route is setting the model, actions, and other specifications
    to be passed into the template for the related feature.
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    ember g route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
  {{#link-to campus.boston}}Boston Campus{{/link-to}}
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
  1. In the first example, product is a nested route under products but the path would
  just be '/:product_id', otherwise the default path would be products/product

  2. In the second example, the path is made to make it look like a nested route
  but there's actually no real communication between 'products' and 'product'
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    [params.id - 1]
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    {{model.data}}
    ```
