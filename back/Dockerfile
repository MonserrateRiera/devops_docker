#Install go
FROM golang:1.16

#Create workdir
WORKDIR /app

#Copy the giles in the conainer
COPY . . 

#Build the project
RUN go build

#Execute the tests
RUN go test ./...

#Expose the port
EXPOSE 8080
#ENV REQUEST_ORIGIN=http://localhost
#Execute the server
CMD [ "./server" ]