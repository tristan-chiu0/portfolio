# Hack 1 - Flaws

## Algorithm Example
### What the heading says is required
The Algorithm section says that an algorithm should integrate sequencing, selection, and iteration to accomplish a task.

### Analysis
The 'calculateAverage' procedure contains sequencing, selection, and minor iteration

### Gaps and Improvements
The 'calculateAverage' procedure has a syntax error, where the output is simply "Expected (, got '{'"
To fix this, replace DISPLAY{"Scores: " + scores} with DISPLAY("Scores: " + scores)
This would improve CPT scoring potential since it allows the code to actually run

The algorithm could also use a way to input scores for a more complex form of iteration. It could ask for the user to input grades with INPUT("Grade: 0 - 100") and continuously ask until the user says STOP. This would improve CPT scoring potential since it makes the iteration user-driven and can actually perform a useful task for people.
`PROCEDURE calculateAverage(numbers)
{
  total ← 0
  count ← 0
  
  FOR EACH num IN numbers
  {
    total ← total + num
    count ← count + 1
  }
  
  IF (count > 0)
  {
    average ← total / count
    RETURN(average)
  }
  ELSE
  {
    RETURN(0)
  }
}

scores ← []

grade ← INPUT("Enter a grade 0-100 (enter STOP to stop):")

REPEAT UNTIL (grade = "STOP")
{
  APPEND(scores, grade)
  grade ← INPUT("Enter another grade 0-100 (enter STOP to stop):")
}

result ← calculateAverage(scores)

DISPLAY("Average score: " + result)
DISPLAY("Scores: " + scores)

IF (result >= 90)
{
  DISPLAY("Grade: A")
}
ELSE
{
  DISPLAY("Grade: B or lower")
}`



