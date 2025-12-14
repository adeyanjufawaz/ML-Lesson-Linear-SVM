# ML-Lesson-Linear(Support Vector Machines(SVM) )
A Support Vector Machine (SVM) is a supervised machine learning algorithm used for classification and regression that works by finding the best boundary between data points.
from sklearn.svm import SVC

# Core Intuition
Think of SVM as a construction worker trying to build a wall between two different types of houses (e.g., Red houses and Blue houses).
1. The Goal: The Widest Street
You don't just want any wall between the groups; you want the safest wall.
2. The Line (Hyperplane): SVM draws a line that separates the two groups.
3. The Safety Gap (Margin): It tries to keep this line as far away from the closest houses on both sides as possible. The wider the gap (margin), the better the model works on new data.

# Support Vectors
Support Vectors: These are the specific houses (data points) that are closest to the line. They are the "pillars" that determine exactly where the line goes. If you move the other houses further back, the line doesn't move. If you move a support vector, the line shifts.

## Types of SVM (Linear vs. Kernel SVM)
The main difference is how they handle complex data.

### 1. Linear SVM (The Straight Cut)
Use this when you can separate your data with a ruler.
How it works: It draws a straight line (or flat plane) through the gap.
Best for: Simple data, like separating "tall people" from "short people" based on height.

### 2. Kernel SVM (The "3D" Trick)
Use this when your data is mixed up in a complex shape (like a ring or a spiral) where a straight ruler won't work.
The Problem: You can't draw a straight line to separate a red ring from a blue center.
The Solution (Kernel Trick): SVM mathematically "lifts" the data from a flat sheet of paper (2D) into the air (3D).
Imagine lifting the blue center dots up. Now you can slide a flat sheet between the raised blue dots and the red dots on the table.
When you look back down at the 2D paper, that flat sheet looks like a curved circle around the blue dots.
