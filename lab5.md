<h1> Lab Report 5 </h1>

For this lab, let's assume a student, Student A asked a question on edstem for help debugging his code.

<b> Title: </b> Having trouble running my bash script


<b> What environment are you using (computer, operating system, web browser, terminal/editor, and so on)? </b>

I'm using a Windows 11 OS on Visual Stuido Code on the bash terminal.

<b> Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”. </b>

I'm trying to make a script that checks the name of a file and returns the file's name as an output. If the file doesn't exist, the output says the file doesn't exist.

<b> Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can. </b>

No matter what I do, it always says the file doesn't exist when it does and it says on line 3 I'm missing ']' when I don't think I am. Here's a screenshot of what I'm talking about.

![image](https://github.com/jlh005/cse15l-lab-reports/assets/130415535/617e0fdf-27fe-4fe0-bb8e-3948af43f5c9)

As you can see, when I try to run the script on "HelloWorld.java" it doesn't work! Both files are in the same directory so I don't think it's a directory problem. Here's the code for HelloWorld.java just in case it's needed.

```
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }
}
```

<h2> TA Response </h2>

Hey Student A, sometimes it's hard to make sense of the error messages the console gives you, but it is right in that there's something wrong with line 3! To make it easier,
remember carefully on what we went over in class, and look over similar bash scripts that we've seen before in class with if statements. What's the major difference
in the if statement of your code and the if statements in class? (Look closely!) 

<h2> Student Response </h2>

Thank you for your response, after looking closely at my code I realized that the error I made was... a typo. I forgot to add spaces before and after the
``'[' and ']'`` 
in my if statement which is why it kept saying that I'm missing ']' in the error statement! 
After adding spaces, my code works correctly now!

![image](https://github.com/jlh005/cse15l-lab-reports/assets/130415535/272280da-576a-4a5c-8ba7-0a80c7001889)


<h2> Reflection </h2>

I've learned alot in the second half of this semester in CSE15l. But the one thing especially is learning how to code bash scripts. It's pretty cool learning how to code
bash scripts and to learn how bash scripts are used to help grade our homework. It's also pretty interesting since I'm taking CSE12 at the same time the differences between
Bash and Java.



