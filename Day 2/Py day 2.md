1.  How many bisections do you expect to need if the tolerance is 10^-3? 10^-6?
10^-9? Explain your reasoning.
    You would expect 10 if the tolernce is 10^-3, 20 for 10^-6, and 30 for 10^-9.  If you run the code, you can see that there are 10 iterations if the tolerance is 10^-3.  If we wish to have a smaller tolerance we need to keep bisecting it.  That would mean that we now want to find the number of times we need to divide the current tolerance by two to get the new one or 10^-3/(2^n) = 10^-6 where n is the number we want.  Solving this we get 9.96 wich rounds to 10.  Thus, for a tolerance of 10^-6 we will need to bisect, or iterate 10 more times than we did for 10^-3.  Following the smae logic, a tolerance of 10^-9 gives an n of 19.93 so we need to iterate 20 more times than we did for 10^-3. 
    
2.  How (aside from actually changing the function in the code) could you
    make bisection.py easier to use for different functions?
    You could place make the bisection a function that took in as arguments the function you want to analyze, the tolerance and the start and end points and make it return the result.  This way if you need the result for a different use you can use this new bisection function as an argument for another function. 

3.  What are the differences between lists and tuples? Tuples and dictionaries? Sets and dictionaries? In what cases might you use each?
Lists are mutable and tuples are immutable, so objects in lists can be modified while tuples' objects cannot.  Similarly, tuples have a fixed length wile lists don't. A dictionary will create lists of values associated with a specific key.  A set in python will also hold a set of values but those values will not be indexed, unlike the lists and tuples.  You can use a tuple for a set of values you do not wish to change or expand, and a list for when you do wish to expand them.  A dictionary might be useful for having several lists saved under specific sub categories, say if you were making a list of usernames and passwords you can have a username key and a password key and lists accordingly.  

4.  How would you check within an if statement if a variable is a list or not?
Why would you need to do this?
mi = ["mama","me","ama"]

word = "me"

def findlista (lista, word):
    if "me" in mi:
        print ("yes")

    else:
        print ("no")

findlista(mi,word)
example of use: if you have a list of usernames for a program and wish to chack an account exist 



    
    
