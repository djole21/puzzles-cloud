|1|2|           
|-|-|            
|3|4|             

text

|a|b|c|d|
|-|-|-|-|
|1|2|3|4|
|e|f|g|h|
|5|6|7|8|

text

|THIS|is|test|table|
|-|-|-|-|
|test|test|test|test|

text

| This | random | test |   |   |   |   |   |   |   |   |   |   |   |   |
|------|--------|------|---|---|---|---|---|---|---|---|---|---|---|---|
|  is  |        |      |   |   |   |   |   |   |   |   |   |   |   |   |
| test |        |      |   |   |   |   |   |   |   |   |   |   |   |   |
|      |        |      |   |   |   |   |   |   |   |   |   |   |   |   |
|      |        |      |   |   |   |   |   |   |   |   |   |   |   |   |
|      |        |      |   |   |   |   |   |   |   |   |   |   |   |   |
|      |        |      |   |   |   |   |   |   |   |   |   |   |   |   |
|      |        |      |   |   |   |   |   |   |   |   |   |   |   |   |
|      |        |      |   |   |   |   |   |   |   |   |   |   |   |   |
|      |        |      |   |   |   |   |   |   |   |   |   |   |   |   |
|      |        |      |   |   |   |   |   |   |   |   |   |   |   |   |
|      |        |      |   |   |   |   |   |   |   |   |   |   |   |   |
|      |        |      |   |   |   |   |   |   |   |   |   |   |   |   |
|      |        |      |   |   |   |   |   |   |   |   |   |   |   |   |
|      |        |      |   |   |   |   |   |   |   |   |   |   |   |   |

text

| Tables   |      Are      |  Cool |
|:---------|:-------------:|------:|
| left |   center      | $1600 |
| col 2|       2       |   $12 |
| c|        3      |    right|

text

| [##]() |        |        |        | [##]() |        | [##]() |        |        |        | [##]() |        | [##]() |        |        |        |        | [##]() |
|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|
| [##]() |        |        |        | [##]() |        | [##]() |        |        |        | [##]() |        | [##]() |        |        |        |        | [##]() |
| [##]() |        |        |        | [##]() |        | [##]() |        |        |        | [##]() |        | [##]() |        |        |        | [##]() |        |
| [##]() |        |        |        | [##]() |        | [##]() |        |        |        | [##]() |        | [##]() |        |        | [##]() |        |        |
| [##]() |        |        |        | [##]() |        | [##]() | [##]() |        |        | [##]() |        | [##]() |        | [##]() |        |        |        |
| [##]() |        |        |        | [##]() |        | [##]() |        | [##]() |        | [##]() |        | [##]() | [##]() |        |        |        |        |
| [##]() |        |        |        | [##]() |        | [##]() |        |        | [##]() | [##]() |        | [##]() | [##]() |        |        |        |        |
| [##]() |        |        |        | [##]() |        | [##]() |        |        |        | [##]() |        | [##]() |        | [##]() |        |        |        |
| [##]() |        |        |        | [##]() |        | [##]() |        |        |        | [##]() |        | [##]() |        |        | [##]() |        |        |
| [##]() |        |        |        | [##]() |        | [##]() |        |        |        | [##]() |        | [##]() |        |        |        | [##]() |        |
| [##]() |        |        |        | [##]() |        | [##]() |        |        |        | [##]() |        | [##]() |        |        |        |        | [##]() |
| [##]() | [##]() | [##]() |        | [##]() |        | [##]() |        |        |        | [##]() |        | [##]() |        |        |        |        | [##]() |
|        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |
| [##]() | [##]() | [##]() | [##]() | [##]() | [##]() | [##]() | [##]() | [##]() | [##]() | [##]() | [##]() | [##]() | [##]() | [##]() | [##]() | [##]() | [##]() |
|        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |

text


| Test case ID | Test Scenario                          | Prerequisites                              | Test data                                                                                                                                                                       | Test Steps                                                                   | Expected results                                                                                                                                                | Actual results                                                                                                                          | Status      | Comments |   |
|--------------|----------------------------------------|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|-------------|----------|---|
| tc_1.1.1     | Testing sign in with gitlab and github | Internet browser                           |                                                                     Use official icons of GitLab and GitHub                                                                     | [Link to sign in/login page](https://staging.puzzlescloud.com/account/login) |                                         1 . Click on provided link  2. See if there are official GitLab and GitHub icons                                        |                                                To see official icons of GitHub and GitLab                                               | As expected |   pass   |   |
|   tc_1.1.2   | Testing sign in with gitlab and github |              Internet browser              |                                    When user wants to sign up with git he will be promoted authorisation dialog that was provided by Git API                                    | [Link to sign in/login page](https://staging.puzzlescloud.com/account/login) |                                                 1. Click on provided link  2. Click on continue with GitLab/hub                                                 |                                     To be promoted authorisation dialog that was provided by Git API                                    | As expected |   pass   |   |
|  tc_1.1.2.1  | Testing sign in with gitlab and github | Internet browser, github or gitlab account |                         if user is already Logged in git hub/lab service we should detect that from the browser and automatically fill user credentials                         | [Link to sign in/login page](https://staging.puzzlescloud.com/account/login) |                   1.Go to your GitLab/Hub account and log in  2. Click on provided link to PuzzlesCloud  2. Click on continue with GitLab/Hub                   |                        To detect that I am logged in with GitLab/hub and to automatically fill in my credentials                        | As expected |   pass   |   |
|   tc_1.1.3   | Testing sign in with gitlab and github | Internet browser, github or gitlab account |                                               User should be informed what information will Puzzles Cloud use from his GIT account                                              | [Link to sign in/login page](https://staging.puzzlescloud.com/account/login) |                   1.Go to your GitLab/Hub account and log in  2. Click on provided link to PuzzlesCloud  3. Click on continue with GitLab/Hub                   | Same as tc_1.1.2.1 ,just to expect to see pop up window provided by PuzzlesCloud that inform us about our information that will be used | As expected |   pass   |   |
|   tc_1.1.4   | Testing sign in with gitlab and github | Internet browser, github or gitlab account | For v1 in pop up that appears when user clicks to sign up user should NOT select repository that he want's to use, he should do that within the app when authorisation is done. | [Link to sign in/login page](https://staging.puzzlescloud.com/account/login) |                   1.Go to your GitLab/Hub account and log in  2. Click on provided link to PuzzlesCloud  2. Click on continue with GitLab/Hub                   |        Pop up shows only informations that will be used, no option to select repository until successful login into PuzzlesCloud        | As expected |   pass   |   |
|   tc_1.1.5   | Testing sign in with gitlab and github | Internet browser, github or gitlab account |                                   When sign up with git is done application should send welcome email to the user and show him dashboard view                                   | [Link to sign in/login page](https://staging.puzzlescloud.com/account/login) | 1. Go to your email that is connected with GIT and check for email from Puzzles cloud  2. Go to puzzles cloud page that you've been redirected after signing in |                                 To see email from PuzzlesCloud and to see dashboard on PuzzlesCloud site                                | As expected |   pass   |   |



   text text




| *test* | **test** | ***test*** | [test](google.com)                                                                                                  | TEST | *TEST* | **TEST** | ***TEST*** |
|-------:|:--------:|------------|---------------------------------------------------------------------------------------------------------------------|------|--------|----------|------------|
|      1 |     1    | 1          | 1.001                                                                                                               |      |        |          |            |
|      2 |     2    | 2          | !@#$%^&*()_+                                                                                                        |      |        |          |            |
|      3 |     3    | 3          | ```````````````                                                                                                     |      |        |          |            |
|      4 |     4    | 4          | ~~~smth~~~                                                                                                          |      |        |          |            |
|      5 |     5    | 5          | ``text``                                                                                                            |      |        |          |            |
|      6 |     6    | 6          | __bold text__                                                                                                       |      |        |          |            |
|      7 |     7    | 7          | ![alt text](https://www.mathworks.com/help/examples/images/win64/BasicImageImportProcessingAndExportExample_01.png) |      |        |          |            |
|      8 |     8    | 8          | ~~The world is flat.~~                                                                                              |      |        |          |            |
|      9 |     9    | 9          |                                                                                                                     |      |        |          |            |
