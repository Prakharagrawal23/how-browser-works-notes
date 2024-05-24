# Browser **(Behind the scene)**

## browser are the software which helps you to talk to the internet and load the html,css,and even js flie from the ***remote server*** and displays them so the browser need to have the remarkable network capability.

## browser is basically an  os

## -0-> Data/memory
## -1-> User Interface
## -2-> Browser Engine - a) Rendering  || b) JS Engine
    - browser need to have the network capability.
    - not only this there are lot more information goes in the browser 
        - timers(js engine don't have the timers so use the timers we have to borrow from the api using the browser)

# How dose browser load the html and display the text or any things on the screen
    const h2Elements = document.getElementsByTagName('h2');
    console.log(h2Elements); 
    only check it we get the nodeList
    we never write the nodeList
## so there comes the rendering- technically we are writing the html but in the end of the day it is understood by c++


# job of the browser is 
    - display the data 
    - interact with the data
# steps for html :-
  - **lode file** - 
  *     1- when browser load any file then it simply see the **raw data**

        2- convert the raw byte in sequence of character(character encoding of html file)

        3 - after the character creation 
            character - generate the tokens from character which is called tokanization(h1,p,html,body) - these take out and save in memory

        4- Relation- we need to create the structure around the tokan

            1--every thing converted into object
            {
                tag: h1,
                title: some,
                data/value: youtube
            }   
            {
                p
            }
            {
                body
            }
            
            2 --- we need to arrenge these object in proper relation 
            - and that conversion of object into the structure that we called as 
            model than the term come (document object model)

        5 -  convert into NodeList - like
           
                      html
                        |
                      body 
                        |
                      |-----|  
                     h1     h2

            (this list of node is given to you by rendering  )

        6 - it give the DOM

# steps for CSS :-
    raw -> character conversion -> tokenization -> created object - relation created -> models

    CSSOM(css object model)

## when the browser lode or see the html file it start working on the DOM but the movement it see the CSSOM it parrally work with cssos but it wort independent to each other

# render tree
    -gather the info - DOM,CSSOM -> browser engine(maths cal done) 
    after this we get the render tree

# painting - in tech term-  when the web page being render to the browser to see it that called as painting

    now we can see the data in page

# javascript part
    when the browser see script tag it will stop executing the dom,cssom or other
    -the preference is js collect the info from js then render the other things


    ( reseachable )
    when dom is not ready but we hit the js part then 

    js -- dom
          (halt until the js file is being read or executed)
    

    when cssom is not ready but we hit the js part

    js    -------     cssom
    (js execution 
    will be halted
    until the cssom 
    is ready )

    (use the async to js will we executed at the end)

