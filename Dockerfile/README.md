
# What is a Dockerfile?

A Dockerfile is a plain text document that contains all the sequential commands a user could call on the command line to assemble a container image.

Docker automatically reads these instructions to build the final image.

## How to Create a Dockerfile

Creating a Dockerfile involves defining a base environment and layering  our application configurations on top of it.

**Essential Prerequisites**

- Install Docker Desktop or Docker Engine.
- Open a terminal or command prompt.
- Prepare your application files in a dedicated project directory.

**Step-by-Step Creation Process**

*1:Create a blank file*

  - Name the file exactly Dockerfile with no extension.
  - Do not use .txt or .json.

*2:Define the base image*
  
  - Use the FROM instruction first.Example:

  - FROM node:18-alpine or FROM python:3.10. 

*3:Set the working directory*
  
  - Use WORKDIR to set the path inside the container.
  
  - Example: WORKDIR /app.

*4:Copy your project files*

  - Use COPY to move local files into the container image.

  - Example: COPY . . copies everything from your local directory.

*5:Install necessary dependencies*

  - Use RUN to execute build-time commands.

  - Example: RUN npm install or RUN pip install -r requirements.txt.

*6:Expose the application port*

  - Use EXPOSE to document the network port.
  
  - Example: EXPOSE 3000.

*7:Define the startup command* 

  - Use CMD to set the default runtime command.

  - Example: CMD ["node", "server.js"] or CMD ["python", "app.py"].

# Standard Example

 Here is how a standard Dockerfile looks for a basic application:


 <img width="333" height="261" alt="image" src="https://github.com/user-attachments/assets/ebf4b6db-a29e-4871-a1ad-ccc772e73413" />


 **Building and Running the Container**
 
 Once your Dockerfile is saved in your project folder, execute these commands in your terminal:

   - Build the image: docker build -t my-app-image .

   - Run the container: docker run -p 8080:8080 my-app-image

<img width="436" height="390" alt="image" src="https://github.com/user-attachments/assets/f0e171fc-1622-4620-8774-291094feea52" />








  
  

  
