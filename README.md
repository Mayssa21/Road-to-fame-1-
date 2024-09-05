import random

class Stage:
    def __init__(self, name, description, challenge):
        self.name = name
        self.description = description
        self.challenge = challenge

class Costume:
    def __init__(self, name):
        self.name = name

class Friend:
    def __init__(self, name):
        self.name = name

class Game:
    def __init__(self):
        self.stages = [
            Stage("Audition", "Your first audition for a small role.", "Perform a monologue"),
            Stage("Supporting Role", "You've landed a supporting role in a TV show.", "Memorize your lines"),
            Stage("Lead Role", "You're the lead actress in a movie!", "Improvise a scene")
        ]
        self.costumes = [
            Costume("Casual Outfit"),
            Costume("Formal Dress"),
            Costume("Costume for a Role")
        ]
        self.friends = [
            Friend("Alice"),
            Friend("Bob"),
            Friend("Charlie")
        ]
        self.current_stage = 0
        self.score = 0

    def play(self):
        print("Welcome to the Actress Journey Game!")
        while self.current_stage < len(self.stages):
            stage = self.stages[self.current_stage]
            print(f"\nStage: {stage.name}")
            print(stage.description)
            self.choose_costume()
            self.meet_friend()
            self.complete_challenge(stage.challenge)
            self.current_stage += 1
        print(f"\nCongratulations! You've become a famous actress with a score of {self.score} points!")

    def choose_costume(self):
        print("\nChoose a costume for this stage:")
        for i, costume in enumerate(self.costumes):
            print(f"{i + 1}. {costume.name}")
        choice = int(input("Enter the number of your choice: ")) - 1
        print(f"You chose: {self.costumes[choice].name}")

    def meet_friend(self):
        print("\nMeet a friend:")
       
