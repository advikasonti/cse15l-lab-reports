# Lab Report 5

## Grading Script

### Writing the Script

To create the grading script from Lab 6, my partner and I simply followed the given instructions from that lab and coded each section step-by-step. 
There were a total of 5 steps to follow with the first one already written. So we had to firgure out the remaining steps on our own.

#### Step 1: Cloning the repository of the student submission to a well-known directory name.
```
CPATH='.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar'

# Step 1:
rm -rf student-submission
git clone $1 student-submission
echo 'Finished cloning'
```
#### Step 2: Checking that the student code has the correct file submitted.
```
# Step 2:
cd student-submission
  if [[ -f ListExamples.java ]]
  then
  echo "ListExamples found"
  else 
  echo "need file ListExamples.java"
  exit 1
  fi
cd ..
```
#### Step 3: Getting the student code and your test file into the same directory.
```
# Step 3:
mkdir grader
cp TestListExamples.java grader
cp student-submission/ListExamples.java grader
cp -r lib grader
```
#### Step 4: Compiling your tests and the student’s code from the appropriate directory.
```
# Step 4:
cd grader
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
if [[ $? -eq 0 ]]
then 
echo "compile succeeds"
else 
echo "compilation error"
exit 1
fi
```
#### Step 5: Run the tests and report the grade based on the JUnit output.
```
# Step 5: 
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples
```
We unfortunately could not figure out how to get the script to report the student's final grade, but we did get the grader to run and to work appropriately for any given student's files.

### Running the Script

To test the script, we ran it on several given files to experiment with various edge cases. All the provided student test file names are listed below followed by the output of the grading script.

#### list-methods-lab3
![Grade1.png](https://raw.githubusercontent.com/advikasonti/cse15l-lab-reports/main/Grade1.png)

#### list-methods-corrected

#### list-methods-compile-error

#### list-methods-signature

#### list-methods-filename

#### list-methods-nested






