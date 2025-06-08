# Projects-Rock-Paper-Scissors-
showcasing previous python work
import random

print("Let's play rock, paper, or scissors")

player_wins = 0
computer_wins = 0

while player_wins < 2 and computer_wins < 2:
  player_choice = input("\nChoose rock, paper, or scissors: ").lower()
  choices = ["rock", "paper", "scissors"]
  computer_choice = random.choice(choices)
  print(f"Computer chose: {computer_choice}")

  if (player_choice == "rock" and computer_choice == "scissors") or (player_choice == "scissors" and computer_choice == "paper") or (player_choice == "paper" and computer_choice == "rock"):
    winner = "Player"
  elif player_choice == computer_choice:
    winner = "Tie"
  else:
    winner = "Computer"

  if winner == "Player":
    player_wins += 1
    print("You won")
  elif winner == "Computer":
    computer_wins += 1
    print("Computer won")
  else:
    print("It's a tie")


  print(f"Current Score - Player: {player_wins}, Computer: {computer_wins}")

  if player_wins > computer_wins:
    print("Congratulations! You won.")
else:
    print("Computer won!")

    import smtplib

def send_email(subject, body, to_email):
    from_email = 'your-email@example.com'
    password = 'your-password'
    with smtplib.SMTP('smtp.example.com', 587) as server:
        server.starttls()
        server.login(from_email, password)
        message = f'Subject: {subject}\n\n{body}'
        server.sendmail(from_email, to_email, message)

send_email('Test Subject', 'This is a test email', 'recipient@example.com')
