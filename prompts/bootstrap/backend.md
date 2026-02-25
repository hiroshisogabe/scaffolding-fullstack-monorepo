<role>
    You are a Senior Fullstack Software Engineer especialized in Node.js and you will bootstrap a backend in this monorepo with minimum viable code.
</role>

<task>Implement a backend in Node.js with mininum viable code</task>

<requirements>
    # Technical

    ## Folder structure
    - Create one specific folder for backend in ./backend.

    ## Project configuration
    - Create a .gitignore with common files and folders which should be ignored, e.g. ./node_modules and .env.
    - Create a real `.env` file in `./backend` with the required variables 
    - Create an .env.example related to the required variables used in the backend implementation for local execution, at minimum `PORT=3000`.

    ## Programming language & web application framework
    - The backend should use Node.js and TypeScript.
    - Express should be the web application framework to serve the API.

    ## Code standards
    - Avoid .js files and consider using .ts whenever it's possible.
    - When using TypeScript, **any as type is not acceptable**.

    ## Server configuration
    - We need to make sure any CORS issues are mitigated in the backend implementation when configuring Express.
    - The Port which will serve the API should be retrieved from a variable from .env file and fallback to 3000 in case it's not present.
</requirements>

<endpoints>
    # Test endpoint

    ## [GET] /test [200]

    ### Possible Status Code
    - 200: Success
    - 500: Unexpected error

    ### Returned payload
    - In case of success, it should contain the properties as the following sample JSON shows:
    {
        "status": 'Running',
        "timestamp": '2026-02-25T13:38:14.406Z'
    }
</endpoints>

<errors>
    # JSON structure
    - The JSON should contain two properties: "error" and "message".
    - The "error" should be the category of the error, e.g. "Data input missing".
    - The "message" should describe the error, e.g. "Name is a required data".

    # Error boundary
    - In case any error occur and wasn't caught, we should return status code 500 with error "Unexpected error" and the original message of the error as the "message".
</errors>

<tests>
    ### Library
    - use jest to run the tests adding any required configuration file. 
    
    ### Path
    - The test files should be in the same path as the main file tested, following the pattern for file name "*.test.*"

    ### Unit tests
    - create unit tests including happy and unhappy paths.
    - every scenario should be considered, e.g. the error boundary scenario.

    ### Real test
    - run the server and make sure it's returning the expected response for a success request at least using curl.
    - report the request url and the response from backend.
</tests>

<critical>
    ### Out of scope

    - **NEVER** create comments in the codebase
</critical>
