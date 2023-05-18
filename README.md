# Mod2 Week2 Assessment - Joe Centeno
5/18/2023

## Setup
1. Fork this repository.
1. Add ONE of the following GitHub profiles as a collaborator to your forked repo:
`memcmahon`, `rtillies`, `zoefarrell`
1. Clone your repo to your local machine.
1. Open your cloned repository in Visual Studio.
1. Insert your name on line 1 to replace `<YOUR NAME HERE>` above.

## Questions (10 Points Possible)
**Important** Answer these questions in this file on your `main` branch.  When finished with the questions, commit and push your main branch.  You do not need to create a pull request yet!

1. What does TDD stand for?
TDD stands for test-driven development. TDD is a way of thinking when approaching a problem in code. The TDD process makes the programmer start with writing a failing test. You then write code relating to your test conditions until your test passes. 

1. What are the three benefits of using TDD?
The first befit to using TDD is having to write a failing test before you write any code. This allows the developer to get an idea of exactly what they need to write since they are setting up the test with conditions based on the desired output. The second befit is being able to iterate on your code when it's not passing a test, this allows the developer to step back and look at the test to determine what to do next. The third befit is that it forces you to write tests, making your code more coverage from bugs. 

1. Imagine you are in an interview.  The interviewer asks: How do you use TDD? How would you answer?
To start off TDD stands for test-driven development. I use TDD when I am approaching a coding problem/project I have not done before. TDD allows me to first create failing tests, making me outline the conditions for the desired output, and TDD allows me to iterate on problem/project code while being able to step back and look at the bigger picture through tests. 

1. For the class below, outline the tests you would need.  Try to use as much C# syntax as possible. The first test has been provided for you. (this question is worth 4 points)
```c#
public class Dog
    {
        public string Name { get; }
        public string Breed { get; }
        public bool IsHungry { get; private set; }

        public Dog(string name, string breed)
        {
            Name = name;
            Breed = breed;
            IsHungry = true;
        }

        public void Eat()
        {
            IsHungry = false;
        }

        public void Sleep()
        {
            IsHungry = true;
        }

        public string Speak()
        {
            return "Bark Bark!";
        }
    }
```
```c#
// Add your tests here

[Fact]
public void DogHasNameAttribute()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    Assert.Equal("Nile", dog.Name);
}

[Fact]
public void DogHasBreedAttribute()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    Assert.Equal("Golden Retriever", dog.Breed);
}

[Fact]
public void DogHasIsHungryAttribute()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    Assert.Equal(true, dog.IsHungry);
}

[Fact]
public void DogCanEat()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    dog.Sleep();

    Assert.Equal(false, dog.IsHungry);
}

[Fact]
public void DogCanSpeak()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    dog.Eat();

    Assert.Equal(true, dog.IsHungry);
}

[Fact]
public void DogCanSleep()
{
    Dog dog = new Dog("Nile", "Golden Retriever");


    Assert.Equal("Bark Bark!", dog.Speak());
}
```

What is a merge conflict, and when might you encounter one?
A merge conflict is when the same file has had multiple changes occur on it at the same time in the same file line. This results in a human having to go through the files and choose what to keep, what's worth manually merging, or what to get rid of. You will most likely encounter merge conflicts when you're working on the same project with others and you all do your pull requests at the same time. 

You and a partner are working on a project together.  Your partner is working on aa-branch; you are working on bb-branch.  In as much detail as possible, describe how you both would get your work combined onto the main branch.
The aa-branch would first submit the pull request for the aa-branch. The owner of the repository would approve the pull request merging aa-branch with the main. The same process would then be done for the bb-branch merging both of them into the main by the end, but making sure to do one pull request before the other.

Why is it good practice to have someone else approve and/or merge your PR?  
It's good practice because it allows the other person to review your code and also make sure that any code that is coming into the main branch is safe/stable code that won't effect main. 

**Before moving on to the next section, commit your work and push your main branch!**
  
## Git Exercise (6 points possible)

1. Create a new branch called `elephants` (1 point)

1. Add the following to the end of the Animal Tracker file:

```
Elephants
- African Savanna
- Asian
- African Forest
```

3. Commit this change to the Animal Tracker file with an appropriate message. (1 point)

1. Create the following files with the listed contents:

**African Savanna.txt**
```
Average shoulder height: 2.6-3.2 meters
Average mass: 3.3-6.6 short tons
```

**Asian Elephant.txt**
```
Average shoulder height: 2.4-2.8 meters
Average mass: 3.0-4.4 short tons
```

**African Forest Elephant.txt**
```
Average shoulder height: 1.8-3.0 meters
Average mass: 2,000-7,000 kilograms
```

5. Add and Commit these new files with an appropriate message. (1 point)

1. Push your `elephants` branch to GitHub. (1 point)

1. Create a Pull Request in GitHub. Write a short description of the changes you made to the repo. (1 point) 

1. Request a review from your collaborator. (1 point)
  
## Submission

Submit the Assessment Submission form linked in your cohort slack channel!

## Rubric

This assessment has a total of 16 Points. Earning 11 or more points is a pass and will indicate that you are progressing well with the material.

As a reminder, this assessment is for students and instructors to determine if there are any areas that need additional reinforcement!
