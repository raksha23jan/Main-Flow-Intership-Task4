query 1: select studentid,Name,(MathScore + ScienceScore + EnglishScore) AS total_score, RANK() OVER (ORDER BY (MathScore + ScienceScore + EnglishScore) DESC) AS student_rank FROM student;
query 2: select studentid,Name,MathScore, SUM(MathScore) OVER (ORDER BY StudentID) AS RunningTotal_MathScore FROM student;
