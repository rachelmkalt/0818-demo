---
title: Building APIs from Scratch with API Designer
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

No OpenAPI specification? No problem! ReadMe's API Designer lets you build your API reference directly in the platform with an intuitive visual interface – no YAML or JSON required.

In this guide, we'll walk through creating a Social Media API with endpoints for listing and creating posts. You'll see how easy it is to document your API even if you're starting from a blank slate.

## Creating Your API Definition

Let's start by setting up the basic structure for your API:

1. Navigate to **API Reference** in your ReadMe project
2. Click the **+ Add** button
3. Select **Start Building** under "Build an API definition from scratch"

<Image align="center" src="https://files.readme.io/bc4cc9a8a3ecb04da38f9424ada388c34b52f178c75edaec6e21d238496730e8-APID_1.gif" />

4. Enter your API definition details:
   * **API Title**: Enter a descriptive name (e.g., "Social Media API")
   * **Target Host URL**: Your API's base URL (e.g., "[http://api.example.com](http://api.example.com)")
   * **Authentication Type**: Select your authentication method (None, API Key, Basic, or Bearer)

<Image align="center" src="https://files.readme.io/e5250c5498b535695c3e50dcea092b277dd9b6aff3160e5afd163313b780c436-APID2.gif" />

5. Click **Save** to create your API definition

Your new API definition will appear in the left navigation panel, ready for you to add endpoints.

## Creating Your First Endpoint (List Social Media Posts)

Let's create an endpoint to retrieve a list of social media posts:

1. In the left navigation, you'll see a default endpoint labeled `/new-endpoint`
2. Rename this to better reflect your API structure - let's call it "Posts"
3. You'll now see this category in your left navigation

<Image align="center" src="https://files.readme.io/4d63568ed316deea36ba2b05220e869707851ee5f3364709ceaf2dd7a96d0fe3-APID3.gif" />

4. Create your GET endpoint for listing posts:
   * Click on the endpoint to edit it
   * Change the title to "List Social Media Posts"
   * Select the **GET** method from the dropdown menu
   * Set the path to `/posts`
   * Add a description explaining what the endpoint does (e.g., "Returns a paginated list of social media posts")

<Image align="center" src="https://files.readme.io/a39fd0ca12dd0c3349cde2b7a24b6fa3157acb04523836e75b275293f4af9ae4-APID_4.gif" />

### Adding Query Parameters

Most list endpoints support pagination or filtering. Let's add some query parameters:

1. Locate the **Query Parameters** section and click the **+** button
2. Add parameters for pagination:
   * Add a `page` parameter of type `integer`
   * Add a `limit` parameter of type `integer`
   * Add any other filtering parameters (e.g., `category` as a `string`)
3. For each parameter:
   * Add a description
   * Set whether it's required
   * Provide a default value if applicable

<Image align="center" src="https://files.readme.io/a1ca60d4e1dbf1daf609a2c9f105dd3142f55968e9601dbbf8df10a5bda3b78a-APID_5.gif" />

### Adding Example Responses

Now let's add an example response to show developers what to expect:

1. Locate the **Add example response** section on the right side
2. Click the **+** button
3. Select the status code (typically `200` for successful GET requests)
4. Add a JSON response example that shows a list of posts with typical fields like IDs, content, timestamps, etc.
5. You can add multiple response examples for different scenarios

<Image align="center" src="https://files.readme.io/cd4bee874e6121586f5c48cde32f860edda6339e933b2179ae3a8f20d2b08943-APID_6.gif" />

## Creating Your Second Endpoint (Create a Social Media Post)

Now let's add an endpoint for creating new posts:

1. In the left navigation, click the **+ New Category** button if you need a new category, or use your existing "Posts" category
2. Click the + icon to add a new endpoint
3. Set up your POST endpoint:
   * Title: "Create New Post"
   * Method: Select **POST** from the dropdown
   * Path: `/posts`
   * Description: "Allows authenticated users to create new posts"

<Image align="center" src="https://files.readme.io/724904d3be8adf197ff4f546730cafd78f0da62a42b5e3eda1cfc8815956e3e2-APID_7.gif" />

### Adding Request Body Parameters

For a POST endpoint, you'll need to define the request body:

1. Locate the **Request Body** section and click to expand it
2. Set the content type to `object`
3. Add the required fields:
   * Add a `content` field of type `string` and mark it as required
   * Add any additional fields your API accepts (e.g., `image_url`, `tags`)
4. For each field:
   * Add a clear description
   * Mark whether it's required
   * Provide any constraints (min/max length, pattern, etc.)

<Image align="center" src="https://files.readme.io/b4383d1a0def59748123b48262d3df72ea33b6f383abb1bfc5d8f8168f25b2e9-APID_8.gif" />

### Adding Request Code Samples

One of ReadMe's powerful features is automatic code sample generation:

1. Find the **Request Code** section on the right
2. ReadMe automatically generates code examples in multiple languages
3. You can also click "Write your own static samples" to add custom examples

<Image align="center" src="https://files.readme.io/0cb7c46e5dbc5176dd5e547878e6e2ac29cfc832fc3fe3eb4644377e21097fd6-APID_9.gif" />

### Adding Example Responses

Finally, add example responses for your POST endpoint:

1. Click the **+** button under "Add example response"
2. Add a `201` status code for successful creation
3. Provide a JSON example of the created resource
4. Consider adding additional response examples for errors like `400` (Bad Request) or `401` (Unauthorized)

<Image align="center" src="https://files.readme.io/9119e28470b379c3b374a6f0426a58127e117b4ffaf7aa041dc5c8709277646e-APID_10.gif" />

## Testing Your API Documentation

After creating your endpoints:

1. Save your changes
2. Toggle to the "View" mode to see how your documentation looks to developers
3. Test the interactive features to ensure your examples work correctly

## Tips for Great API Documentation

* **Be thorough with descriptions**: Clearly explain what each endpoint does and why
* **Provide realistic examples**: Use example data that looks like real-world usage
* **Document error states**: Include examples of error responses and how to handle them
* **Use consistent naming**: Maintain a consistent style across all endpoints and parameters
* **Add "What's Next"**: Use the "What's Next" section to guide users on related endpoints they might need

By following this guide, you've created a well-documented API reference from scratch using ReadMe's API Designer. Your developers now have interactive, clear documentation that helps them integrate with your API quickly and easily.

Remember, you can always return to the API Designer to add endpoints, update parameters, or enhance your documentation as your API evolves.

## Currently Unsupported OpenAPI Features

We currently don't support all OpenAPI features in our API Designer. If you use any of these features in an endpoint you will be unable to edit them in our UI. However, these endpoints will still render properly in the documentation and can still be updated by editing the OpenAPI file directly.

<br />

| Unsupported OpenAPI Feature | Explanation                                                                                                                                                                               | OpenAPI Documentation                                                                                                                      |
| --------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Additional Properties       | The additionalProperties keyword is used within a schema to define whether properties not explicitly defined in the schema are allowed in objects, and if so, what their types should be. | [Dictionaries, HashMaps and Associative Arrays](https://swagger.io/docs/specification/v3_0/data-models/dictionaries/)                      |
| Callbacks/Webhooks          | OpenAPI has a feature to define endpoints that will make an API call once an event has completed.                                                                                         | [Callbacks](https://swagger.io/docs/specification/v3_0/callbacks/)                                                                         |
| References                  | Any endpoint that defines an object using a $ref.                                                                                                                                         | [Using Ref](https://swagger.io/docs/specification/v3_0/using-ref/)                                                                         |
| Common Parameters           | Endpoints where parameters are defined at the path level instead of the method, so the parameters are shared between all methods for that URL.                                            | [Describing Parameters](https://swagger.io/docs/specification/v3_0/describing-parameters/#common-parameters)                               |
| Links                       | Links are an OpenAPI feature that describes how the responses of one endpoint can be used as input for other operations.                                                                  | [Links](https://swagger.io/docs/specification/v3_0/links/)                                                                                 |
| Polymorphism                | Polymorphism lets you define a schema that can represent multiple types or models.                                                                                                        | [Inheritance and Polymorphism](https://swagger.io/docs/specification/v3_0/data-models/inheritance-and-polymorphism/?sbsearch=Polymorphism) |
| Server Variables            | Variables can be defined in the base path which can have a preset list of values the user can choose from.                                                                                | [API Server and Base Path](https://swagger.io/docs/specification/v3_0/api-host-and-base-path/?sbsearch=server%20variables)                 |
| Style                       | The Style keyword allows configuration on how multiple values should be passed to a parameter.                                                                                            | [Parameter Serialization](https://swagger.io/docs/specification/v3_0/serialization/?sbsearch=Styles)                                       |
| XML                         | Endpoints that accept or respond with XML data.                                                                                                                                           | [Representing XML](https://swagger.io/docs/specification/v3_0/data-models/representing-xml/?sbsearch=xml)                                  |
