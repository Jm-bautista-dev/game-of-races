# game-of-races
#a python program where you can choose what race you want to choose and you can use their own skills
class wizzard:
    def __init__(self):
        self.first_skill = ("magic circle ice blast")
        self.second_skill = ("magic circle hellfire of dragon warrior")
        self.ultimate = ("through heaven and earth bare witness. the shrine of last monk")

    def show_skills(self):
        return(self.first_skill, self.second_skill, self.ultimate)

    
class rouge:
    def __init__(self):
        self.first_skill = ("thief of midgard")
        self.second_skill = ("bloody flash of assassin")
        self.ultimate = ("domain expansion: instant kill ")

    def show_skills(self):
        return(self.first_skill, self.second_skill, self.ultimate)


class archer:
    def __init__(self):
        self.first_skill = ("raging arrow of archangel")
        self.second_skill = ("raining arrow meteor")
        self.ultimate = ("thunder flash: the arrow of tartarus")

    def show_skills(self):
        return(self.first_skill, self.second_skill, self.ultimate)

class main:
    def __init__(self):
        print("1. WIZZARD")
        print("2. ROUGE")
        print("3. ARCHER")
        choice = input("choose a combatant: ")

        if choice == "1":
            self.combatant = wizzard()
            print("you choose a WIZZARD")
        elif choice == "2":
            self.combatant = rouge()
        elif choice == "3":
            self.combatant = archer()
        else:
            print("invalid input enter only (1 to 3)")
            return
        
        self.choose_skill()

    def choose_skill(self):
        while True:    
            print("press Q for first skill")
            print("press W for second skill")
            print("press E for ultimate")
            skill = input().lower()

            if skill == "q":
                print(self.combatant.first_skill)
            elif skill == "w":
                print(self.combatant.second_skill)
            elif skill == "e":
                print(self.combatant.ultimate)
            else:
                print("invalid input please enter only (q w e)")
                return
        
main()
