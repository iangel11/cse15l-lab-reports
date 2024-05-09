# Lab3 Report
For this Lab Report, I would like to choose `ArrayExamples.java` from week 4's lab.

### `A failure-inducing input:`
#### This is a JUnit test that demonstrates a failure when an array contains multiple occurrences of the lowest value, in this case, it's '3'.

` 
@Test
    public void testFailureAverageWithoutLowest() {
        double[] input = {3, 3, 7, 9}; // Two '3's, which are the lowest
        double expected = 8.0; // Should be (7 + 9) / 2
        assertEquals(expected, ArrayExamples.averageWithoutLowest(input), 0.001);
    }
`


![Image](cdNoArg.png)
