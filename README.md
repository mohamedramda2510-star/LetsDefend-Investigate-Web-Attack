LetsDefend – Investigate Web Attack

1. Lab Overview

- Platform: LetsDefend
- Lab Name: Investigate Web Attack
- Category: Web Security / Log Analysis
- Log Source: "access.log"
- Focus: Web Attack Investigation
- Status: Completed

2. Scenario

The organization detected suspicious web attacks and requested a deeper investigation.

The objective was to analyze the Apache access logs, identify the attacker's reconnaissance activities, investigate different attack techniques, and determine whether any attacks were successful or involved persistence attempts.

3. Investigation Findings

The investigation revealed multiple attack activities:

- Web Reconnaissance: Nikto automated scanning tool.
- Directory Discovery: Directory brute force.
- Third Attack Type: Brute force.
- Third Attack Successful: Yes.
- Fourth Attack Type: Code Injection.
- Payload: "whoami"

Persistence Investigation

A suspicious payload indicating a possible persistence attempt was identified:

%27net%20user%20hacker%20asd123!!%20/add%27

Decoded payload:

'net user hacker asd123!! /add'

This command attempts to create a local Windows user account named "hacker".

4. Questions & Answers

Q1. Which automated scan tool did the attacker use for web reconnaissance?

Answer: "nikto"

Evidence:

<img width="922" height="405" alt="Screenshot 2026-11-21 145101" src="https://github.com/user-attachments/assets/cd398c94-612f-4b58-b0f1-cd9b08c479d0" />


---

Q2. After web reconnaissance activity, which technique did the attacker use for directory listing discovery?

Answer: "Directory brute force"

Evidence:

<img width="957" height="436" alt="Screenshot 2026-11-21 150542" src="https://github.com/user-attachments/assets/af5a7974-42ee-4b15-8b04-72a60b767195" />


---

Q3. What is the third attack type after directory listing discovery?

Answer: "brute force"

Evidence:

<img width="959" height="432" alt="Screenshot 2026-11-21 150634" src="https://github.com/user-attachments/assets/858dc6a1-f9ae-4bf4-ab0e-585296edf42c" />


---

Q4. Is the third attack successful?

Answer: "yes"

Evidence:

<img width="506" height="277" alt="Screenshot 2026-11-21 151456" src="https://github.com/user-attachments/assets/c0f14334-09eb-421b-92d8-d63cace13c96" />

---

Q5. What is the name of the fourth attack?

Answer: "Code Injection"

Evidence:

<img width="959" height="410" alt="Screenshot 2026-11-21 150829" src="https://github.com/user-attachments/assets/d2736e29-21d0-43bd-bf78-79f0e95199bb" />


---

Q6. What is the file payload for this attack?

Answer: "whoami"

Evidence:


<img width="948" height="402" alt="Screenshot 2026-11-21 150030" src="https://github.com/user-attachments/assets/11a9bbe6-c798-4b6a-8ad4-391dc1826f84" />


---

Q7. Is there any persistence clue for the victim machine in the log file? If yes, what is the related payload?

Answer:

%27net%20user%20hacker%20asd123!!%20/add%27

Evidence:

<img width="956" height="416" alt="Screenshot 2026-11-21 145937" src="https://github.com/user-attachments/assets/e4d4edd6-86f6-41c0-a56a-fa50865859d9" />


---

5. Key Takeaways

- Analyzing web server access logs.
- Identifying automated reconnaissance using Nikto.
- Detecting directory brute-force activity.
- Investigating brute-force and code injection attacks.
- Analyzing suspicious HTTP payloads.
- Identifying potential persistence attempts.

6. Conclusion

Successfully completed the LetsDefend Investigate Web Attack challenge.

This lab improved my practical skills in web log analysis, identifying multiple attack techniques, investigating suspicious HTTP requests, and recognizing potential persistence activity.

Skills: Web Log Analysis | Apache Access Logs | Nikto | Brute Force | Code Injection | Incident Investigation | Blue Team
