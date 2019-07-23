# When to user Docker

Docker is a tool that you can use for creating, deploying and running applications with containers.
It is used to tackle difficulties with multiple different operating systems and architectures.
Docker uses virtualization so developer can package up an application with all dependencies and run
the application on any operating system that can run Docker. Using Docker can also be answer for many security
challenges.

## When to use it?

 - When you want to run multiple applications and want to keep them separated.
 - When you develop application by using different environments or with team.
 - When your application needs to go throught multiple development phases.

## Benefits of using Docker

 - Docker makes scaling you application easier.
 - Isolated containers make your application usually more secure.
 - Deploying your application for different environments will be faster and easier.
 - Addin more dependencies for your application is usually more faster.
 - Using Docker will eliminate problems with different versions of software since you will specify it with Docker.

## Example of containers

For example we could have web application with frontend and backend. 
Backend has a list of random quotes and returns single one when it's called.
Frontend has only visuals and ability to request single quote from backend and show it for users.

When running backend and frontend inside same operating system they could now have any problems with each other,
for example dependency of same program but different versions. And if either one crashes operating system, the whole thing would be down.

When using containers we can isolate frontend and backend inside different containers and each one with their own dependencies.
And if either one crashes container, the host machine could still be running.