🔄 Flowchart for Password Generation

+----------------------------+
| Start                     |
+----------------------------+
           |
           v
+----------------------------+
| Input: password length    |
+----------------------------+
           |
           v
+----------------------------+
| Is length < 4?            |
+----------------------------+
     |Yes           |No
     v               v
+----------------+  +------------------------------+
| Raise ValueErr |  | Define character sets:       |
| (length too short) | lowercase, uppercase, digits,|
+----------------+  | and symbols                  |
                    +------------------------------+
                               |
                               v
              +---------------------------------+
              | Randomly pick 1 char each from  |
              | lowercase, uppercase, digits,   |
              | and symbols                     |
              +---------------------------------+
                               |
                               v
          +-----------------------------------------+
          | Fill remaining characters randomly from |
          | the combined set of all characters      |
          +-----------------------------------------+
                               |
                               v
              +-----------------------------+
              | Shuffle the password chars  |
              +-----------------------------+
                               |
                               v
              +-----------------------------+
              | Join chars into a string    |
              +-----------------------------+
                               |
                               v
              +-----------------------------+
              | Return generated password   |
              +-----------------------------+
                               |
                               v
                          +---------+
                          |  End    |
                          +---------+


---

🧠 Explanation of Each Step

1. Input

User can specify the desired password length. Default is 12.

If the length is less than 4, a ValueError is raised because at least one character from each category (lowercase, uppercase, digit, symbol) is required.


2. Character Set Definition

The function uses the string module to get:

ascii_lowercase → a–z

ascii_uppercase → A–Z

digits → 0–9

punctuation → special characters like !@#$%^&*()...



3. Initial Character Selection

One character from each category is selected to ensure password diversity and strength.


4. Remaining Characters

The remaining characters (length − 4) are randomly chosen from the combined set of all types.


5. Shuffling

The list of characters is shuffled to ensure the required characters are in unpredictable positions.


6. Return Password

All characters are joined into a single string and returned.





