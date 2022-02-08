# PaulCamper offline challenge

This project is about a tranlation service to translate text from one language to another.

For translation a 3rd party is used. To save the costs of the third party this service needs to implement some optimization tasks.
Below are the optimizations applied.

1. retry requests N times with exponential back off before failing with an error
2. cache request results in the storage to avoid charges for the same queries (use simplest inmemory storage)
3. deduplicate simultaneous queries for the same parameters to avoid charges for same query burst

## Steps to use this repo
1. Clone this repo to your local
2. run this command to download all packages "go get -u ./... -v"
3. to run the code type "go run ."
4. to run the test type "go test"
