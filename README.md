# Cgpa-calculator-
#include <iostream>
using namespace std;
//  make extranal function to optmise the codeA
float calculateCGPA(int semesters) {
    float semGPA, sum = 0;

    for(int i = 1; i <= semesters; i++) {
        cout << "Enter GPA of Semester " << i << ": ";
        cin >> semGPA;
        sum += semGPA;
    }

    return sum / semesters;
}

int main() {
// input the coureses
    int n;
    cout << "Enter number of Subject: ";
    cin >> n;

    float grade;
    float credit;
    float total_Credits = 0;
    float total_GradePoints = 0;

    for(int i = 1; i <= n; i++) { // introducing loop for taking grade point and credits hours
        cout << endl<<"Subject"<< i << endl;
        
        cout << "Enter Grade Point: ";
        cin >> grade;

        cout << "Enter Credit Hours: ";
        cin >> credit;

        total_Credits = total_Credits + credit;
       total_GradePoints = total_GradePoints + (grade * credit);
    }
// perform computation for GPA
    float GPA = total_GradePoints / total_Credits;
    // print total  grade points
       // print total  credit
          // print GPA semester

    cout << "\nTotal Credits: " << total_Credits;
    cout << "\nTotal Grade Points: " << total_GradePoints;
    cout << "\nSemester GPA: " << GPA;

    // CGPA calulation by using functiom
    int semesters;
    cout << "\n\nEnter total number of semesters: ";
    cin >> semesters;
    float CGPA = calculateCGPA(semesters);// call function

cout << "Final CGPA: " << CGPA;
return 0;
