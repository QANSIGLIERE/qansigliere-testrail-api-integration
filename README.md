# qansigliere-testrail-api-integration

The main idea of ​​this library created in the JavaScript language is to provide a ready-made set of API methods for
integration with Testrail

## Author

https://www.youtube.com/@QANSIGLIERE/

## Installation

Using npm `npm i qansigliere-testrail-api-integration`

## How to use it

### Create a \*.env file

Create any \*.env file (like `testrail.env`) and write the following information in the created file

```
export TESTRAIL_URL="__YOUR_TESTRAIL_URL__"
export TESTRAIL_USERNAME="__YOUR_TESTRAIL_EMAIL__"
export TESTRAIL_APIKEY="__YOUR_TESTRAIL_APIKEY__"
```

### Make the \*.env file works

Just run in the terminal the following command: `source yourfile.env`

### And now You can make any API call to Your TestRail

```
var { TestRail_API } = require('qansigliere-testrail-api-integration');

(async function Demo() {
    let new_integration = new TestRail_API();
    let resp = await new_integration.get_templates(1);
    console.log(JSON.stringify(resp));
})();
```

## API Documentation

### Case Types

TestRail documentation is present [here](https://support.testrail.com/hc/en-us/articles/7077295487252-Case-Types)

#### get_case_types

```
let new_integration = new TestRail_API();
let resp = await new_integration.get_case_types();
```

### Roles

TestRail documentation is present [here](https://support.testrail.com/hc/en-us/articles/7077853258772-Roles)

#### get_roles

```
let new_integration = new TestRail_API();
let resp = await new_integration.get_roles();
```

### Statuses

TestRail documentation is present [here](https://support.testrail.com/hc/en-us/articles/7077935129364-Statuses)

#### get_case_statuses

```
let new_integration = new TestRail_API();
let resp = await new_integration.get_case_statuses();
```

#### get_statuses

```
let new_integration = new TestRail_API();
let resp = await new_integration.get_statuses();
```

### Templates

TestRail documentation is present [here](https://support.testrail.com/hc/en-us/articles/7077938165780-Templates)

#### get_templates

```
let new_integration = new TestRail_API();
let resp = await new_integration.get_templates(1);
```

### Priorities

TestRail documentation is present [here](https://support.testrail.com/hc/en-us/articles/7077746564244-Priorities)

#### get_priorities

```
let new_integration = new TestRail_API();
let resp = await new_integration.get_priorities();
```

### Result Fields

TestRail documentation is present [here](https://support.testrail.com/hc/en-us/articles/7077871398036-Result-Fields)

#### get_result_fields

```
let new_integration = new TestRail_API();
let resp = await new_integration.get_result_fields();
```

### Runs

TestRail documentation is present [here](https://support.testrail.com/hc/en-us/articles/7077874763156-Runs)

#### get_run

```
let new_integration = new TestRail_API();
let resp = await new_integration.get_run(1);
```

#### get_runs

```
let new_integration = new TestRail_API();
let resp = await new_integration.get_runs(1);
```

#### add_run

```
let new_integration = new TestRail_API();
let resp = await new_integration.add_run(1, {
    suite_id: 3,
    name: 'Generated by QANSIGLIERE',
    description: 'Created for DEMO',
    include_all: true,
});
```

#### update_run

```
let new_integration = new TestRail_API();
let resp = await new_integration.update_run(2, {
    description: 'A description for the test run',
    include_all: true,
});
```

#### close_run

```
let new_integration = new TestRail_API();
let resp = await new_integration.close_run(2, {});
```

### delete_run

```
let new_integration = new TestRail_API();
let resp = await new_integration.delete_run(2, {});
```

### BDDs

TestRail documentation is present [here](https://support.testrail.com/hc/en-us/articles/7832161593620-BDDs)

#### get_bdd

```
let new_integration = new TestRail_API();
let resp = await new_integration.get_bdd(5);
```

#### add_bdd

```
let new_integration = new TestRail_API();
let resp = await new_integration.add_bdd(
    1,
    `@APP-1
Feature: Users cannot login with invalid credentials
The login page should not allow users to login with invalid credentials, and it should not reveal sensitive info relating to the correctness of credentials.Background:Given I am viewing the login page`);
```

### Case Fields

TestRail documentation is present [here](https://support.testrail.com/hc/en-us/articles/7077281158164-Case-Fields)

#### get_case_fields

```
let new_integration = new TestRail_API();
let resp = await new_integration.get_case_fields();
```

#### add_case_field

```
let new_integration = new TestRail_API();
let resp = await new_integration.add_case_field({
    "type": "Multiselect",
    "name": "my_multiselect",
    "label": "My Multiselect",
    "description": "my custom Multiselect description",
    "configs": [
        {
            "context": {
                "is_global": true,
                "project_ids": ""
            },
            "options": {
                "is_required": false,
                "items": "1, One\n2, Two"
            }
        }
    ],
    "include_all": true
});
```

## Related Videos

-   https://youtube.com/live/q2NO23ruDqI?feature=share
-   https://youtube.com/live/IC4hoYwzvDY?feature=share
-   https://youtube.com/live/o9yonQpeFg4?feature=share
-   https://youtube.com/live/qjw5o0Kk6iQ?feature=share
