# What is Container ?

Container is box (bluePrint) . It used the host  operating system . Container has not own operating system .

Container is a  isolated  lightweight box that has everything  your app needs to run   but  share the heavy system  parts with computer 
it runs on 

In this box or container  all requirments or dependencies  for an application exist that is necessry to run  application  in any environment or laptop

This box has diffrent dependencies of application according to  application  like OS , language version ,libraries  ,database etc.

## How we build the docker container ?

To build a Docker container, you need a configuration file called a Dockerfile. 

This file acts as a blueprint that tells Docker exactly how to package your code and its required dependencies.

Here is a step-by-step example using a simple Node.js web application.

***1: Create the Docker Blueprint***

Create a text file named exactly Dockerfile (no file extension) in the same folder as your code.Here we try  to containerize the Nod.js application.


<img width="462" height="296" alt="image" src="https://github.com/user-attachments/assets/8dfdbe9e-097c-4efb-9b9e-988361b8320c" />


***2. Commands to Build and Run***

- Build the container image:
   docker build -t my-first-container .
- Run the container:
 docker run -p 3000:3000 my-first-container

Once running, you can open your web browser and type http://localhost:3000
to see your containerized app in action   

# What is Virtulization ? 

Virtualization is a technology that uses software to create simulated or virtual versions of physical computer hardware

including Server Virtualization, Storage Virtualization, and Network Virtualization. 

It allows one physical machine to run multiple independent virtual systems at the same time.

**How It Works**

- Uses a special software layer called a hypervisor.
  
- The hypervisor connects directly to physical hardware or sits on a host operating system.

- It divides core resources like CPU, memory, and storage into isolated virtual machines (VMs).

- Each VM runs its own operating system and apps just like a real computer

  <img width="440" height="296" alt="image" src="https://github.com/user-attachments/assets/7806fb0f-75a0-48ac-bae4-647254905ea5" />
