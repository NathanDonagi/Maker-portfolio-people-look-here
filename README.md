I choose to highlight lines 29-82 in the ScaleCode.ino file in my analytical balance repository in my GitHub. Can be found at https://github.com/NathanDonagi/Analytical-Balance/blob/main/ScaleCode/ScaleCode.ino for ease of finding.

The code itself is incredibly rough and not my best work, but the idea behind of using a binary search in a physical machine context I feel was one of my single brightest moments. For context I was attempting to make an analytical balance which balanced out the weight of a mass by running voltage through a magnet. From the examples I could find online they mostly appeared to use either analog voltage feedbacks or PID loops to adjust the voltage to find the exact cutoff. I lacked the circuit parts to use analog feedback and due to the limitations of my Arduino and specific peculiarities of the magnets force output the PID switched between being either underdamped or settling on the wrong value (not in a way a higher integral term could fix).

The code segment therefore represents my solution to my dilemma. By using a binary search and checking discrete voltage values I can avoid aforementioned headaches and get an exact output voltage precise to 2^16 bits.


Here is a lift of the repositories containing the code for each project shown in my video in order:
https://github.com/NathanDonagi/Analytical-Balance,
https://github.com/NathanDonagi/Roomba-Discord-Bot,
https://github.com/NathanDonagi/Google-App-Script-Unblocker,
https://github.com/NathanDonagi/A-Trot-Through-Time,
https://github.com/NathanDonagi/Itsy-Bitsy-Robot