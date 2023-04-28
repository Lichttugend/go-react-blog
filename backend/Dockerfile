# Use the official Golang image as a base image
FROM golang:1.20.1

# Set the working directory
WORKDIR /app

# Copy go.mod and go.sum files
COPY go.mod go.sum ./

# Download all dependencies
RUN go mod download

# Copy the rest of the code
COPY . .

# Build the Go app
RUN go build -o main .

# Expose the port the app runs on
EXPOSE 8080

# Run the app
CMD ["./main"]
