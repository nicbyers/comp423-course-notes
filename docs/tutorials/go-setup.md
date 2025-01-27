# Setting up a dev container for Go

* Primary author: [Nicholas Byers](https://github.com/nicbyers)
* Reviewer: [Brian Bordeaux](https://github.com/bbounc)

## Prerequisites
Before you begin, make sure you have the following tools installed on your machine:
- **Docker**: To run the development container.
- **Visual Studio Code**: The editor you'll use to write your Go code.
- **Dev Containers extension for VS Code**: This allows you to work inside a containerized environment with all necessary tools pre-installed.

## Steps for setting up the DevContainer:

### 1. **Create a new directory**
Start by creating a new directory for your Go project and navigating to it in your terminal:

**mkdir go-dev-container**
**cd go-dev-container**

### 2. **Initialize a git repository**
Initialize a new git repository inside your project directory:

git init

### 3. **Set up your DevContainer**
Setting up a devcontainer allows you to work inside a container with GO pre-installed. Create a .devcontainer directory and add the following devcontainer.json file: 

{
  "name": "Go Dev Container",
  "image": "mcr.microsoft.com/vscode/devcontainers/go",
  "extensions": [
    "golang.go"
  ]
}

### 4. **Verify Go installation**
Once your DevContainer is set up, open the project folder in Visual Studio Code and let the DevContainer build. You can verify that Go is correctly installed by running the following command in the VS Code terminal:

go version 

It should output something similar to:

go version go1.19.3 linux/amd64


### 5. **Create a basic "Hello COMP423" program**
Create a file named main.go in the project directory and add the following code: 

package main

import "fmt"

func main() {
    fmt.Println("Hello COMP423")
}

### 6. **Build and run the program**
To run the program, you can use the go run command:

go run go/main.go (because main.go is in the go folder, you use the "/")

This will execute the program and output:
Hello COMP423

### 7. **Conclusion**
You've successfully set up a Go project inside a DevContainer, written a basic "Hello COMP423" program, and learned how to run and build it.

To ensure your work is saved and shared with your team, you can push your changes to your GitHub repository. Here’s how:

Stage your changes: Before pushing, make sure to stage your files:

  git add .

Commit your changes: Commit the changes with a meaningful message, for example:

  git commit -m "Completed Go Project with Hello COMP 423 program."

Push to GitHub: Push your changes to your remote repository on GitHub:

  git push -u origin <meaningful-name>


Your project is now ready to be developed further, and you can continue to use the DevContainer for a consistent development environment.