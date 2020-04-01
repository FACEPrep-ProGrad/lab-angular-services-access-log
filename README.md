![Image description](https://i1.faceprep.in/ProGrad/face-logo-resized.png)

# ProGrad Lab | Access Log
## Introduction

We have been hired by a local sports club to create a system that allows the manager to control who accesses the team's locker room. They are going to add a device next to the door, and everyone will have to write who they are and why they are in the locker room.

## Learning Goals

After this lesson, you will be able to:

- Create an angular service to share information with all the components in your application.
- Create an angular form to insert new data in the service.

## Requirements

- Fork this repo.
- Clone this repo.

## Submission

Upon completion, run the following commands:

```bash
$ git add .
$ git commit -m "done"
$ git push origin master
```

Navigate to your repo and create a pull request from your master branch to the original repository's master branch.

In the pull request name, add your Prograd id, name, and last name separated by a dash "-".

## Deliverables

You need to generate the starter code and fill it with the necessary code to satisfy the requirements described below.


## Starter Code

To generate the starter code, follow the steps given below

- To create a new application,
    - Open your ubuntu or cmd terminal and execute the following command
      - ```ng new app-name```
      - for example, ng new super-wars
    - To create a new component, execute the command 
      - ``` ng generate component component-name```
      - example, ng generate component contacts
      
## How to run

- To run the project go to your ubuntu terminal or VScode editor
    - open the ubuntu or cmd terminal or inside the vscode editor
    - run the command following command
    - ```ng serve --open or ng serve -o```
    
## Deliverables

All the files of your project, including the service and the different components you will use to create your solution.

## Progression 1: Service creation

First of all, we are going to create an Angular Service to keep our access log. We will use an Array of objects to do that. In this array, each object will store the following information:

- `person`, a string indicating who is accessing the locker room.
- `message`, a string to indicate what they are doing in the locker room.
- `createdAt`, a date field to know what day and time has the person accessed to the locker room.

We will also add two different methods to interact with the array defined in the service:

- `getAccessLog()` that will return the array.
- `addAccessItem()`, that will add an item to the array with the two parameters it will receive:
  - `person`
  - `message`

**Don't forget to export the service to be able to use it in other parts of the application.**

**Tasks**

- Create `AccessControlLog` Service.
- Declare a `logMessages` array of objects. Each object will have the following information:
  - `person`, string.
  - `message`, string.
  - `createdAt`, date.
- Define an `addAccessItem()` method, receiving two parameters:
  - `person`.
  - `message`.
- Define a `getAccessLog()` method, that returns the array of objects.

## Progression 2: Form Component

We are going to need a form to insert new access items in the Service array. We are going to create a `LogFormComponent` component to have all the form functionality on it. The form will have two different fields: `person` and `message`.

Once the component is created, we have to add the Service as a provider, so we can interact with the methods we created. When the form is submitted, we have to call the `addAccessItem()` method in the service to add a new element to the array.

**Before save, you have to be sure that both fields contain information, so remember to use form validations.**

**Tasks**

- Create a `log-form` component.
- Add the `AccessControlLog` Service as a provider.
- Create the HTML form in the component.
- Handle the button event to call the `addAccessItem()` method in service.
- Once the log is created, show a message in the screen indicating that the registration was successful.
- Use form validations to avoid errors.
- **Style the form!** Remember we are working for a professional sports team, we have to do our best work here.

### Progression 3: Show the registers

The access log information is supposed to be secret. No one will be able to see the whole log. But we want to be sure that everything is working fine, so we have to show the whole list of logs somehow.

After a person registers, we will show the list in the browser's console. It's easy, you have to iterate over all the elements in the array and show the information with `console.log`.

**Tasks**

- After each insertion, get all the elements in the array and show them in the console.

Happy Coding ProGrad ❤️
