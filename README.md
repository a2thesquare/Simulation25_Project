# Simulation25_Project


Project description

❗ The simulation project submission deadline is 17 December 2025 at 23:59. To be able to submit, you must be part of a group on Moodle, either with another teammate or by yourself. You can join a group via this link. The submission should be an archive (e.g., zip) containing your code in a Jupyter Notebook file (.ipynb extension), a PDF document with your complete answers (including any plots), and a PDF/PPT with your final presentation. Grading will be done based on the answer PDF; the notebook is mainly for any extra validation or cross-checking results. You can submit at this link.

❗ The corresponding presentations are on 18 December 2025 between 10:15 and 12:00 in UniMail room D017. Your presentation should be around 7 minutes long, with another 7 minutes for questions. You can claim a slot using this link.

## Closed Queuing network simulation (17 pt)
Build a simulator to capture the following system and answer the questions below. A total of N=40 jobs circulate in different parts of the systems: CPU, disk, and resting area. There is one CPU and two disks, one slow and one fast. Each job starts at the CPU station and takes an average of 2 seconds. After CPU, a job fetches the data from the disk, needing an average of 3000 disk cycles. There are two possible choices of disks, fast and slow, which have a speed of 1000 cycles per second and 100 cycles per seconds, respectively. After the disk station, the job can rest for 15 seconds on average. The figure below gives an overview of the system:

The choices of distributions are up to you. You are welcomed to try different distributions to answer the following questions and assess the impact of different variants.

<img width="380" height="267" alt="image" src="https://github.com/user-attachments/assets/73f26326-7a51-4a0e-aac6-53f113737c31"/>

### Questions:
(3p) What will be the maximal system throughput in terms of number of jobs, given two different load balancing strategies for sending jobs between the fast and slow disk? You need to come up with two load balancing strategies and compare them. \
(3p) What will the system throughput and average response time of a job be if a faster CPU is used? Say, CPU time is reduced to 1 seconds on average and the rest of the system remains the same.\
(3p) What will the system throughput and average response time of a job be if a second fast disk is added? Again, you need to compare the throughput under two different load balancing strategies.\
(3p) What will the system throughput and average response time of a job be if a faster CPU is used and a second fast disk is added? And, you use the better load balancing strategies out of two you propose in the first question?\
(5pt) If you can answer all the above questions with different number of N and plot them in the following style:

<img width="536" height="214" alt="image" src="https://github.com/user-attachments/assets/b8da1062-c220-4474-8d83-435dbd35ce7c"/>



## Open Queuing network simulation (8 pt)
The second part of the project is to make an open-queuing network simulator, where the jobs arrive from the outside following Poisson processes with the rate of lambda. The system is shown as the following figure:

Each job needs to go to the CPU, following an exponential distribution with a mean of 10 jobs per second, and then proceeds by either one of the disks. There are two disks, each of which has an exponentially-distributed processing time. The fast disk has a processing rate of 12 jobs per second and the slow disk has the rate of 9 jobs per second. The number of buffer spaces in each queue is infinite.

<img width="364" height="214" alt="image" src="https://github.com/user-attachments/assets/e5b8dbf6-cbca-4b9a-bcc4-9d0d3709d6d2"/>

### Questions:
(4pt) Use your simulator to find the maximum sustainable throughput of such a system in terms of number of jobs. Support your answer with simulation results. \
(4pt) Find out the average response times for following cases over three arrival rates of your choice: case (i) - a single queue in front of fast and slow disk; case (ii) - a separate queue for each disk, jointly applying the shortest queue load balancing strategy when sending the jobs from the CPU to disk. \

<img width="402" height="153" alt="image" src="https://github.com/user-attachments/assets/f94a3873-db1d-4283-94b2-c158df84595d"/>

