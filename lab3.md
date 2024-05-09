# Lab3 Report
For this Lab Report, I would like to choose `ArrayExamples.java` from week 4's lab.

### `A failure-inducing input:`
#### This is a JUnit test that demonstrates a failure when an array contains multiple occurrences of the lowest value, in this case, it's '3'.

    @Test
    public void testFailureAverageWithoutLowest(){
        double[] input = {3, 3, 7, 9};
        double expected = 8.0; // Should be (7 + 9) / 2
        assertEquals(expected, ArrayExamples.averageWithoutLowest(input), 0.001);
    }


### `Non-Failure-Inducing input:`
#### This JUnit test shows a case where the code works as expected because there is only one occurrence of the lowest value, which is '4'.
    
    @Test
    public void testSuccessAverageWithoutLowest() {
        double[] input = {4, 6, 8, 10}; // '4' is the lowest and unique
        double expected = 8.0; // Should be (6 + 8 + 10) / 3
        assertEquals(expected, ArrayExamples.averageWithoutLowest(input), 0.001);
    }



### `The symptom, as the output of running the two tests:`

![Image](twoTest.png)
