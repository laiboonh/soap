# Sample SOAP endpoint server

## Start Server

`./gradlew bootRun`

## Query server using curl (without proxy)

`curl --user spike:spike123 --header "content-type: text/xml" -d @request.xml https://localhost:8443/ws -k | xmllint --format -`

## Query server using curl (with proxy http->https)

`curl --user spike:spike123 --header "content-type: text/xml" -d @request.xml http://localhost:8000/ws -k | xmllint --format -`

## Query for wdsl

`curl --user spike:spike123 https://localhost:8443/ws/countries.wsdl -k | xmllint --format -`