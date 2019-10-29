# Hm2

class Student:

    def __init__(self,ID,firstName,lastName,gender,birthdate,gradeHW,gradeParticipation,gradeQuiz,gradeFinal):
        self.ID = ID
        self.fullName = firstName + lastName
        self.email = firstName + lastName + "@aua.am"
        self.gender = gender
        self.birthdate = birthdate
        self.gradeParticipation = gradeParticipation
        self.gradeHW = gradeHW
        self.gradeQuiz = gradeQuiz
        self.gradeFinal = gradeFinal

    def getPersonalInfo(self):
        print(self.ID)
        print(self.fullName)
        print(self.email)
        print(self.gender)
        print(self.birthdate)
        print("__________________________")
    def getCurrentGrade(self):
        print(self.fullName)
        print("HW: ",self.gradeHW,"%")
        self.gradeHW = (self.gradeHW*0.15)
        print("Participation: ",self.gradeParticipation,"%")
        self.gradeParticipation = (self.gradeParticipation*0.15)
        print("Quiz: ", self.gradeQuiz,"%")
        self.gradeQuiz = (self.gradeQuiz*0.30)
        print("Final: ", self.gradeFinal,"%")
        self.gradeFinal = (self.gradeFinal*0.40)
        self.fullGrade = round(self.gradeHW+self.gradeQuiz+self.gradeParticipation+self.gradeFinal)
        print("Full Grade: ",self.fullGrade,"%")
        print(" )))) ")

def main():
    st1 = Student("AUA123", "Davit", "Ispiryan", "M", "01/01/2000", 54, 88, 77, 78)
    st2 = Student("AUA456", "Rafael", "Hayruni", "F", "01/01/2000", 53, 93, 65, 88)

    st1.getPersonalInfo()
    st2.getPersonalInfo()
    st1.getCurrentGrade()
    st2.getCurrentGrade()

main()
