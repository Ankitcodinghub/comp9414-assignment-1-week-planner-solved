# comp9414-assignment-1-week-planner-solved
**TO GET THIS SOLUTION VISIT:** [COMP9414 Assignment 1-Week Planner Solved](https://www.ankitcodinghub.com/product/comp9414-artificial-intelligence-solved-2/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;120156&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;COMP9414 Assignment 1-Week Planner Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
More technically, this assignment is an example of a constraint optimization problem, a problem that has constraints like a standard Constraint Satisfaction Problem (CSP), but also a cost associated with each solution. For this assignment, you will implement a greedy algorithm to find optimal solutions to these scheduling problems that are specified in a file. However, unlike the greedy search algorithm described in the lectures on search, this greedy algorithm has the property that it is guaranteed to find an optimal solution for any such problem (if a solution exists).

A CSP for this assignment is a set of variables representing activities, binary constraints on pairs of activities, and unary constraints (hard or soft) on activities. The domains are all the combinations of days ‘sun’, ‘mon’, ‘tue’, ‘wed’, ‘thu’, ‘fri’ and ‘sat’, and times ‘7am’, ‘8am’, ‘9am’, ‘10am’, ‘11am’, ‘12pm’, ‘1pm’, ‘2pm’, ‘3pm’, ‘4pm’, ‘5pm’, ‘6pm’ and ‘7pm’. So the possible values are day time pairs such as ‘mon 9am’. Each activity name is a string of letters or numbers (with no spaces).

The possible input (tasks and constraints) are as follows:

# activities with name and duration activity hnamei hdurationi

# binary constraints

constraint hA1i before hA2i # A1 ends when or before A2 starts

constraint hA1i after hA2i # A1 starts after or when A2 ends

constraint hA1i starts hA2i # A1 and A2 start at the same day and time

constraint hA1i ends hA2i # A1 and A2 end at the same day and time

constraint hA1i overlaps hA2i # A2 starts after A1 starts and not after A1 ends,

# and ends after A1 ends

constraint hA1i during hA2i # A1 starts after A2 starts and ends before A2 ends

constraint hA1i equals hA2i # A1 and A2 start and end at the same day and time

constraint hA1i same-day hA2i # A1 and A2 start and end on the same day

# hard domain constraints

domain hAi on hdi # A starts (and ends) on day d

domain hAi before hdi # A starts (and ends) before day d

domain hAi after hdi # A starts (and ends) after day d

domain hAi starts-before hti # A starts at or before time t on any day

domain hAi starts-after hti # A starts at or after time t on any day

domain hAi ends-before hti # A ends at or before time t on any day

domain hAi ends-after hti # A ends on or after time t on any day

# soft domain constraints

domain hAi around hti hcosti # cost per hour of not meeting time preference t

The time difference between t1 and t2 (converted to integer hours) is simply the absolute value of t1 − t2, denoted |t1 − t2|. Then, where cv is the soft constraint applying to variable v:

cost(S) = Pcv∈C costcv ∗ |tv − tcv|

Heuristic

In this assignment, you will implement greedy search using a priority queue to order nodes based on a heuristic function h. This function must take an arbitrary CSP and return an estimate of the distance from any state S to a solution. So, in contrast to a solution, each variable v is associated with a set of possible values (the current domain).

h(S) = Pcv∈C mintv∈dom(v) costcv ∗ |tv − tcv|

Implementation

Use the Python code for generic search algorithms in searchGeneric.py. This code includes a class Searcher with a method search() that implements depth-first search using a list (treated as a stack) to solve any search problem (as defined in searchProblem.py). For this assignment, extend the AStarSearcher class that extends Searcher and makes use of a priority queue to store the frontier of the search. Order the nodes in the priority queue based on the cost of the nodes calculated using the heuristic function, but making sure the path cost is always 0. Use this code by passing the CSP problem created from the input into a searchProblem (sub)class to make a search problem, then passing this search problem into a Searcher (sub)class that runs the search when the search() method is called on this search problem.

You should submit weekPlanner.py and all other files from AIPython needed to run your program. The code in weekPlanner.py will be run in the same directory as the AIPython files that you submit. Your program should read input from standard input (i.e. not hard-coded from input1.txt) and print output to standard output (i.e. not hard-coded to output1.txt).

Sample Input

Below is an example of the input form and meaning. Note that you will have to submit at least three input test files with your assignment. These test files should include one or more comments to specify what scenario is being tested.

Print the output using Python’s standard print function as a series of lines, giving the start day and time for each activity (in the order the activities were defined) and the cost of the optimal solution. If the problem has no solution, print ‘No solution’ (with capital ‘N’). When there are multiple optimal solutions, your program should produce any one of them. Important: For auto-marking, make sure there are no extra spaces at the ends of lines, and no extra empty lines after the cost is printed (i.e. no additional newline characters after the one on the last line of the solution showing the cost). This is the standard behaviour of the Python print function. Set all display options in the AIPython code to 0.

The output corresponding to the above input is as follows:

Submission

• Submit all your files using the following command (this includes relevant AIPython code):

give cs9414 ass1 weekPlanner.py search*.py csp*.py display.py *.txt

• Your submission should include:

– Your .py source file(s) including any AIPython files needed to run your code

– At least three input files used to test your system (including comments to indicate the scenarios tested), and the corresponding output files (call these input1.txt, output1.txt, input2.txt, output2.txt, etc.); submit only correctly formatted input files

• When your files are submitted, a test will be done to ensure that your Python files run on the CSE machine in the 9414 environment; take note of any error messages

• Check that your submission has been received using the command:

9414 classrun -check ass1

Assessment

Assessment Criteria

• Correctness: Assessed on valid input tests as follows, where input is read from a file redirected to standard input, and output is redirected to standard output (not hard-coded file names):

python3 weekPlanner.py &lt; input1.txt &gt; output1.txt

• Programming style: Understandable class and variable names, easy to understand code, good reuse of AIPython code, adequate comments, suitable test files

Appendix: AIPython Classes
