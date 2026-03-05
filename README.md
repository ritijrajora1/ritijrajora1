
## 🌐 Socials:
[![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?logo=Instagram&logoColor=white)](https://instagram.com/ritijrajora) [![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/ritij-rajora-9591a83ab) [![email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:ritijrajora021@gmail.com) 

# 💻 Tech Stack:
![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white) ![Power Bi](https://img.shields.io/badge/power_bi-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
# 📊 GitHub Stats:
![](https://github-readme-stats.vercel.app/api?username=ritijrajora1&theme=dark&hide_border=false&include_all_commits=true&count_private=false)<br/>
![](https://nirzak-streak-stats.vercel.app/?user=ritijrajora1&theme=dark&hide_border=false)<br/>
![](https://github-readme-stats.vercel.app/api/top-langs/?username=ritijrajora1&theme=dark&hide_border=false&include_all_commits=true&count_private=false&layout=compact)

<!-- Proudly created with GPRM ( https://gprm.itsvg.in ) -->
import random

print("Welcome to the Number Guessing Game!")
print("I am thinking of a number between 1 and 100.")

number = random.randint(1, 100)
guess = None
attempts = 0

while guess != number:
    guess = int(input("Enter your guess: "))
    attempts += 1

    if guess < number:
        print("Too low! Try again.")
    elif guess > number:
        print("Too high! Try again.")
    else:
        print("Congratulations! You guessed the number in", attempts, "attempts.")
