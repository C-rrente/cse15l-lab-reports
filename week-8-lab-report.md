# Week 8 Lab Report

```
rm -rf student-submission
git clone $1 student-submission

mv student-submission/ListExamples.java .

javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java

if [ $? -gt 0 ]
then
        echo "fail" + $1 > grades
fi

java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples

if [ $? -gt 0 ]
then
        echo "fail" + $1 >> grades
else
        echo "pass" + $1 > grades
fi
```      

# Compile Error
![image](https://user-images.githubusercontent.com/71531248/203903241-767e4511-c29f-4830-9e6b-39d4ceed573a.png)

# Methods Corrected
![image](https://user-images.githubusercontent.com/71531248/203903483-f9194579-2cdc-4023-a74e-3064dd44c39b.png)

# Methods Signature
![image](https://user-images.githubusercontent.com/71531248/203903691-4727fed4-876e-42ea-acfe-5a37d053978d.png)


# Compiler Error
For this method, my script compiles the code, puts it in the correct directory, then checks if it compiled, if it didn't then it files and adds the failure to the grades file.
It then runs the code and checks to see if the code passes the tests, if it does not, it adds another failure, otherwise adds a pass.
