# Lab3 Report

## Part 1
For this Lab Report, I would like to choose `ArrayExamples.java` from week 4's lab.

### `A failure-inducing input:`
#### This is a JUnit test that demonstrates a failure when an array contains multiple occurrences of the lowest value, in this case, it's '3'.

    @Test
    public void testFailureAverageWithoutLowest(){
        double[] input = {3, 3, 7, 9};
        double expected = 8.0; // It should be (7 + 9) / 2
        assertEquals(expected, ArrayExamples.averageWithoutLowest(input), 0.001);
    }


### `Non-Failure-Inducing input:`
#### This JUnit test shows a case where the code works as expected because there is only one occurrence of the lowest value, which is '4'.
    
    @Test
    public void testSuccessAverageWithoutLowest() {
        double[] input = {4, 6, 8, 10}; 
        double expected = 8.0; // It should be (6 + 8 + 10) / 3
        assertEquals(expected, ArrayExamples.averageWithoutLowest(input), 0.001);
    }



### `The symptom, as the output of running the two tests:`
#### As shown in this screenshot, the test designed to verify failure handling has indeed failed, while the other test passed.

![Image](Screenshot 2024-05-08 at 10.14.46 PM.jpg)

### `The bug, before-and-after`
#### Particularly in `ArrayExamples.java`, the bug is situated in the `averageWithoutLowest` method.

Here's the original code: 

    static double averageWithoutLowest(double[] arr) {
        if(arr.length < 2) { return 0.0; }
        double lowest = arr[0];
        for(double num: arr) {
          if(num < lowest) { lowest = num; }
        }
        double sum = 0;
        for(double num: arr) {
          if(num != lowest) { sum += num; }
        }
        return sum / (arr.length - 1);
    }


And, here's that code after the fix:

    static double averageWithoutLowest(double[] arr) {
        if(arr.length < 2) { return 0.0; }
        double lowest = arr[0];
        int lowestCount = 0;
        for(double num: arr) {
          if(num < lowest) {
            lowest = num;
            lowestCount = 1;
          } 
          else if (num == lowest) {
            lowestCount++;
          }
        }
        double sum = 0;
        for(double num: arr) {
          sum += num;
        }
        return (sum - lowest * lowestCount) / (arr.length - lowestCount);
    }


### `Explanation of the fix`
####This fix adapts the same logic as before but uses different numerical examples. By counting all occurrences of the lowest number, we ensure the mean is calculated only over the numbers that aren't the lowest, correctly adjusting for multiple instances of the lowest value. This revised example maintains the integrity of the initial solution while providing a unique test scenario and numbers.
