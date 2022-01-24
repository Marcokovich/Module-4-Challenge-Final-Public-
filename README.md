# Pycity Schools
## 1. Project Overview
### Background
The School board has notified Maria that the data for their schools' testing score has been altered. That the testing scores for Thomas High School 9th Graders’ exam scores for Math and Reading show signs of alterations. They have tasked Maria to handle this instance of academic dishonesty. She has tasked us with nullifying the scores of the students entangled in the academic dishonesty (The entire 9th grade class of Thomas High School.
### Purpose
This code is to read the data from a .csv file into a data frame, set the scores of the 9th grade class of Thomas High School to NaN(Null), and perform an analysis of the district scores. The demonstrations in this code include functions, utilization of Pandas and Numpy, and the manipulation of data frames to make this report.
## 2. Results
#### Student count at Thomas High School remained unaltered, but scores have been recalculated with the 461 students removed
### District Summary
- The district summary shows a minimal change, this makes sense since its only 461 students were removed from a population of 39170
  - Although this is due to the formatting and rounding shenanigans, the only change observable is a .1 change in Math score averages.

unaltered:

![image](https://user-images.githubusercontent.com/71575748/150702614-9fa3ccb3-6d16-42e7-8522-9cdb9e276423.png)

with NaN:

![image](https://user-images.githubusercontent.com/71575748/150702636-78a8b9aa-f216-4246-a7f9-33dc68b39348.png)

### School Summary
- The per school summary sees a more noticeable change
  - However, the sample size is smaller, and the formatting has more sig figs.
  - we observe an increase in Math score average and passing percentage, but a decrease in Reading score average and passing percentage
  - This leads to a decrease in overall passing percentage
    - These changes occur in every observation to the same degree, given its the only change in the data.

unaltered:

![image](https://user-images.githubusercontent.com/71575748/150703001-1248bc0f-5470-4ae4-b611-a3266f323458.png)

with NaN:

![image](https://user-images.githubusercontent.com/71575748/150703030-b819ecc2-c8da-4596-942a-d595c808ee54.png)

### Relative Performance
- Replacing the scores had no effect on Thomas High Schools comparative ranking since replacing the scores led to an increase in overall passing percentage. 
  - Increases in average Math scores and Math passing percentage
  - Decreases in average Reading scores, Reading passing percentage, and overall score.

unaltered:

![image](https://user-images.githubusercontent.com/71575748/150703304-53c65215-89b4-4f5d-813b-057a2d9b821f.png)

with NaN:

![image](https://user-images.githubusercontent.com/71575748/150703326-7c64d51e-468c-458f-8b71-fe2d0808291a.png)

### Math and Reading Scores by Grade
- Math Scores change significantly from being a number to being null.

unaltered:

![image](https://user-images.githubusercontent.com/71575748/150704530-982d59b0-2128-44e3-93a8-4d744841fe3b.png)


with NaN:

![image](https://user-images.githubusercontent.com/71575748/150704493-0bf26073-c69b-4928-abf7-4a509bfcc237.png)

- Reading Scores undergo a similar change

unaltered:

![image](https://user-images.githubusercontent.com/71575748/150705002-f8189933-102e-49f1-8ac4-e82eda34184d.png)

with NaN:

![image](https://user-images.githubusercontent.com/71575748/150705022-4fe33b51-6cdd-45c0-ae7c-8e716afea207.png)

### Scores by school spending
- In the spending bins, there is no change in the scores, but in the unformatted scores we see very small, insignificant changes. (highlighted bin contains THS)
  - Increases in average Math scores and Math passing percentage
  - Decreases in average Reading scores, Reading passing percentage, and overall score.

unaltered:

![image](https://user-images.githubusercontent.com/71575748/150705397-03b4c159-e1cf-4c2b-8e4d-8d9e174a6090.png)

with NaN:

![image](https://user-images.githubusercontent.com/71575748/150705417-f73150c6-5789-463b-9098-b9dc2cc9fa5d.png)

### Scores by school size
- In the Scores by size the change is once again only noticeable in the unformatted version. (highlighted bin contains (THS)
  - Increases in Average Math scores and Math passing percentage
  - Decreases in Average Reading scores, Reading passing percentage, and overall score.

unaltered:

![image](https://user-images.githubusercontent.com/71575748/150705743-0b7a5da6-d3c5-4c21-8496-a979d0c280f1.png)

with NaN:

![image](https://user-images.githubusercontent.com/71575748/150705763-13ba8769-9e37-4ec4-b890-7abb32f0f69e.png)

### Scores by school type
- In scores by school type, we have a similar change akin to size and funding. Too small to catch in formatted summary. (highlighted bin contains (THS)
  - Increases in average Math scores and Math passing percentage
  - Decreases in average Reading scores, Reading passing percentage, and overall score.

unaltered:

![image](https://user-images.githubusercontent.com/71575748/150706312-afb1e0df-931a-48c6-940e-c9ad4f7b8487.png)

with NaN:

![image](https://user-images.githubusercontent.com/71575748/150706339-9c531eb4-f2c1-455b-8927-6446087d3818.png)

## 3. Summary
1. Small change in math scores for the district when formatted.
2. unform changes observed:
  - Increase in Math scores
  - Decrease in Reading scores and overall scores 
3. Minor change in Thomas High School scores
4. We see a tiny change in the Scores by spending, so small it's only noticeable in the unformatted summary
5. In school size we see a similar change, so small you need more sig figs
6. In the type of school we see the same slight changes.
- Given the population size, and the fact that we're looking at a subset of a subset, it makes sense that we wouldn't see significant change.
