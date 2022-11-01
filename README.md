# -DS-542-Week-8-Assignment

## University 

class University:
  def __init__(self,university_name,location, undergraduate_students, graduate_students):
    self.university_name = university_name
    self.location = location
    self.undergraduate_students = undergraduate_students
    self.graduate_students = graduate_students
    
  def print_university_size(self)  :
      
      print("The sum of the attributes undergraduate_students and graduate_students " + str(self.undergraduate_students+self.graduate_students))
      
      
  def is_undergraduate_greater(self) :
      
      if self.undergraduate_students > self.graduate_students:
          print( "There are more undergraduate students than graduate students")
          
      else:
          print("There are more graduate students than undergraduate students")
      
SPU = University('Saint Peter’s University',"United States",50,60)
SPU.print_university_size()  
SPU.is_undergraduate_greater() 


## College

class College(University):
    def __init__(self,university_name,location, undergraduate_students, graduate_students,state):
        University.__init__(self, university_name,location, undergraduate_students,graduate_students)
        self.state = state
        
    def print_college(self) :
        print("The university "+ self.university_name)
        print("The State of University is "+ self.state)

SPU = College('Saint Peter’s University',"United States",50,60,"New Jersey")
SPU.print_university_size()  
SPU.is_undergraduate_greater()  
SPU.print_college()
