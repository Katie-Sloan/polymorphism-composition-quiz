# Polymorphism & Composition Homework - Quiz

# Polymorphism

1. What does the ___word___ 'polymorphism' mean?

It means that something can take many shapes/forms.  

2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.

It means that an object can have more than one type. For example, let's imagine a Newspaper class and a Tablet class. They might both implement an interface called INews, which contains a method for displaying news stories. This would mean that a newspaper could either behave as a Newspaper object or an INews object, and a tablet could either behave as a Tablet object or an INews object.

3. What can we use to implement polymorphism in Java?

Interfaces and abstract classes are good ways to implement polymorphism.   

4. How many 'forms' can an object take when using polymorphism?

There is no limit to this, because although a class can only have one super class, it can implement as many interfaces as it wants.

5. Give an example of when you could use polymorphism.

Let's imagine a Guitar class and a Singer class. Both the Guitar Class and the Singer class implement an interface called IMakeMusic. IMakeMusic has a method called makeMusic(), which returns a string called "music". 

The Guitar Class needs to fulfil the contract created by the IMakeMusic interface, meaning the Guitar Class needs to contain a method called makeMusic(). The Guitar class might therefore have a makeMusic() method which returns a string of different chords, for example "C D G C". 

Similarly, a singer might also implement the IMakeMusic interface. It might have a slightly different makeMusic() method, for example one which returns a string of lyrics.  

Whilst a singer and a guitar both share the behaviour of making music, they have different properties - for example, a guitar has strings, a singer does not. A guitar has a brand, a singer does not. This means that it would not make sense to use inheritance here and it is better to use an interface because it means that when the singer wants to sing, or the guitar wants to play a song, they can each do so by "morphing" from Guitar and Singer objects, respectively, into IMakeMusic objects.        

# Composition

6. What do we mean by 'composition' in reference to object-oriented programming?
Composition describes a "HAS A" relationship (unlike inheritance which describes an "IS A" relationship).

7. When would you use composition? Provide a simple example in Java.
You would use composition where you are dealing with two or more objects which connect with each other, but which are not really similar. For example, a film would have a director, and also a script. The director and a script are connected in that a film HAS both of these things - but a film, a director and a script do not share all of the same properties. So, you could use composition here. You would achieve this by having a Film Class, with the director and script as properties of the class. You would then have a Director Class and a Script Class which define the properties/methods which a director object and a script object would have.     

8. What is/are the advantage(s) of using composition?
Composition is a very useful way of making classes work together, and it is a lot more flexible than using inheritance. With inheritance, sub classes are weighed down with all of the properties and methods which their super classes have. This may not always be appropriate (for example, a guitar/singer share some common behaviours but it would not be DRY, or even make sense, for the singer to inherit all of the properties of the guitar). Composition is really helpful here because it means we can cherry-pick the objects that we want our classes to be composed of, without being restricted or weighed down by inheriting all of the properties of a super class. So, a guitar might have a top note that it can reach, and so might a singer. Composition might be used to give both the guitar and the singer a "top note" property which might be an instance of the Notes Class. 

9. When an object is destroyed, what happens to all the objects it is composed of?

The class from which the objects were instantiated will remain, but the objects themselves will be destroyed.