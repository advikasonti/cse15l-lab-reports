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






