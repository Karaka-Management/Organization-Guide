# Episode 1

## Introduction

Hi my name is Dennis and I'm the creator of the Orange-Management organization. I decided to create a vlog about the project I'm working on it's vision, progress, problems as well as solutions because I believe this could be an interesting journey for myself and maybe some other developers.

My main occupation is controlling and finances with a love for software development since I'm probably 14 years old. I'm sure I will do an episode where I talk a little bit about myself if it becomes relevant for the topics that I want to cover.

## Table Of Contents

However in this episode I will talk about what the Orange-Management organization and what it's respective project are trying to achieve.

## The Project

The Orange-Management project is about creating a web application which allows an organization to handle most of it's activities in this very application which includes for example businesses, educational institutes, healthcare and non-profit organizations.

Generally speaking there are tons of tools out there which support you with very specific tasks for any of these purposes but at one point you will realize that you have to spent a large amount of effort in working with so many different tools or integrating them into each other. Also more and more tools feel like they are primarily focusing on buzzwords and marketing instead of actually solving the key problems.

The vision of Orange-Management is to provide benefits which drastically improve productivity and reduce unnecessary friction which is present in many modern software almost like it is a key selling-point for them. I'm not only talking about web applications which seem to get slower and slower but also native desktop software. I've worked with different CRMs, ERPs, Finance software, Intranet Software and so on and the amount of frustration I personally and also various other people I worked together with feel is insane. Slow user interface feedback is probably the least critical in many tools while still being annoying but the amount of missing quote on quote features, which I think should belong to the core software, is mind-boggling. It's like software is developed without feedback by the end-users who have to live and use these tools on a daily basis.

I also belief modern software should be available to end-users at reasonable pricing models which becomes harder and harder to achieve for small to mid-sized organizations if you consider that many services and applications cost $10 and upwards per licence per month. If you have a couple of organization members and different services you need to use, this becomes really expensive real quick and prevents small to mid-sized organization to use a decent range of modern tools because they simply can't afford it.

I could probably go on and on about where I think other software solutions fail but it's probably better to explain my goals and let everyone for themselves decide if what I'm trying to achieve this is at least from a conceptual point of view better or not.

## Goals

The goals of the project are:

1. The focus is on the solution of the problem
2. The solutions must be financially attractive for a very wide range of end-users
3. Provide solutions to a wide range of problems so that the amount of necessary third party tools gets reduced to the absolute minimum
4. Multiple solutions must be well integrated into each other for reduced friction and seamless workflows
5. Accessible for everyone from everywhere. This means usable on desktop, tablet and phone, for people with disabilities, online/offline usage, and all of this with simple user interfaces that have a modern feeling
6. Fast user interface feedback and good performance overall. No one likes software where you don't know what it is doing and if you can continue to work or need to wait for the application to respond

With these key goals I hope to create software that can help as many people as possible to increase their productivity, reduce their frustration with software and reduce the amount of mundane tasks that should be handled by software.

## How to achieve

And now lets come to how I belief to achieve these goals.

### 1. Solution

Focusing on the solution of a problem is done by using the software actively during development. By using it problems become frustrating and I'll be forced to fix them, I actually experience it myself instead of only getting feedback from other users. Additionally feedback from other users is integrated in order to get a wider spectrum of opinions. The important part is that the feedback comes from real end-users. Since my strength lies within business operations as I am a business controller and now head of finance the business solutions are getting implemented first. My background allows me personally to make design decisions which other developers have little knowledge about.

### 2. Costs

In order to keep the costs for small- and mid-sized companies low the application is structured in modules. End-users are able to select those modules which they need for managing their organization. It is important that these modules will be priced reasonably in order to prevent piling up costs. Another idea is to combine certain modules together and create packages at low prices for different purposes. What other effects the modular system will have will be covered at a later point. The exact pricing model will be checked later after the application is mostly finished in order to have a better basis for this decision. However the goal is to make it attractive even for small organizations which I belief should be supported rather than ignored.

A very important aspect is that the pricing will be completely transparent beforehand. Users will know how much they will have to pay without making an inquiry like many other business applications do nowadays. At the same time there will also be demos for different use cases online accessible by everyone which is also very unusual compared to other business facing software where you have to request a demo. I belief that if you truly think you a have a great product, then you don't need to hide its costs and your product in general behind annoying contact and inquiry forms. The product should mostly speak for itself without the need of a sales or marketing person promoting it.

### 3. Functionality

My personal business background allows me to implement and design a very wide range of modules and functionality because I know most of the workflows and tasks that stand behind them. The key driver is probably my own frustration with existing software solutions and the desire to create a great tool that can help other people. The wide range of functionality will be achieved by implementing the tools and features in modern organization management software that my colleagues at work and I hope to see every day. After the initial development phase more and more opinions from a wide range of users will be collected and evaluated. I belief that while third party tools can provide very comprehensive features they sometimes lose focus of what's really important for the end-user and what kind of core problem they should try to solved.

### 4. Integration

Integrating different solutions is done by simply creating them as first class citizens. By developing the majority of solutions instead of using third party tools or APIs it becomes much easier to integrate and maintain them in one seamless application. Every module knows how the core application is working and how one module may use features of another module. Because every module uses the same core framework and application all modules are on the same playing field and can be nicely tied together while it's still possible to use them individually.

Well designed APIs of course provide similar benefits but there is no overall system in place which combines and integrates them into each other. The way this application is built makes it feel like everything is one big software while in reality it is a collection of modules which simply follow the same basic idea "Give the user the impression he is using one piece of software".

### 5. Accessibility

In terms of Accessibility the term "mobile first" became a very common expression for websites and web applications. I want to go away from this term as the application will not be designed first anything. The development will try to achieve the best experience for every individual platform. Just because an application should look good on mobile doesn't warrant to reduce the desktop user experience and vice versa.

The layout and design will be the hardest for me personally to achieve because my strength is not in the aesthetic compartment. This is also why I am implementing functionality first and only do minor design and layout work currently.

The application will not use an existing framework for JavaScript or CSS which will result in a lot of additional work but I belief the end result will give the user a much better experience as almost everything is built for this very project instead of using available generalized solutions which are then customized.

The offline usability will be a major feature I hope to achieve but the core focus in the beginning will be the online usage. For the offline usage I'm fairly certain that this can be implemented at a later stage semi easily through service workers and smart middleware in some key frontend parts.

### 6. Performance

The feeling of good performance can achieved by giving the users feedback about their input as fast as possible so that the user knows what is happening and doesn't have to guess if he can continue to work or needs to wait for the application.

Actual good performance will be achieved through a custom slim backend framework which focuses on the task at hand and offloads requests if necessary instead of using generalized solutions which may do too much work for the specific use case I need. That being said it may come at a surprise when I say that for now I've chosen to do most of the backend development in PHP.

For those people who have not already closed the browser window after hearing that I will create an episode later on where I will focus on explaining some of the key decisions I've taken which also includes the programming language. Early disclaimer the programming language is one of those key decisions which is most likely going to change at one point in the far future.

## Current Status

In order to give you a very quick impression of the current status let me tell you that some very important core functionalities are already implemented which allow me to draft a decent amount of things but there is still a long way to go until a first version with a handful of modules can be released to some external test candidates. Currently most of the drafting is done based on the needs and requirements of myself and the two companies I'm working for.

### Drafted Key Components

* The state of the frontend framework is very early on as only very basic UI interactions are possible
* The backend framework is probably the most developed part of the application as most key functions such as basic routing, dispatching, database queries, http requests and responses and more are already implemented to a point where they can be used.
* The core application is also at a decent development status. It's possible to install and load modules, handle user permissions and propagate views with model data
* The rudimentary build process and test suit is already setup which allows to test large amounts of the application and to setup the dev environment
* Some modules are drafted and although these modules are far from finished they at least help with checking the requirements for the interfaces and core application

### Missing Key Components

As already stated the least developed parts are frontend related but also the project website and some key backend components such as caching. The development process still has a very long way to go but I feel like I'm at a point where I can start to show certain aspects and make progress videos which might be kind of fun to watch.

## Sample Screenshots

On these screenshots you can see some modules loaded and the current UI state of the project. Obviously screenshots are barely an indication of the status of a project yet I still think they can give you a first impression. I can not mention it enough but the frontend is something that still needs the most work done so please try to think of the layout only as first sketches and nothing more.

For the next videos I will probably go into the editor and browser instead of creating a screencast but for this introduction video I felt like doing a screencast would be the better solution.

## Next Episodes

In the next episode I will go into the backend framework and show how it works and use its most important components. The best way to do this is probably by creating a small random application which doesn't have anything to do with this project in particular.

The 3rd episode will show you how a module is created and installed in the application. For that purpose I will create a new sample module and install it.

The 4th episode will be about the backend and API application which are already setup by going through them and probably creating a new standalone application for the module we created in the previous episode.

The 5th episode is all about how to setup the dev environment, use tests and the build scripts.

In the 6th episode will explain the current status of the project, issue tracking and next steps.

Later I intend to do episodes about key changes and implementations that I consider worth to talk about. Another important video I intend to do at some point is about the key project decisions such as programming language, business strategy future services and so on.

However that's it for this video, thank you for watching maybe you'll continue to follow me on my journey and have a great day.