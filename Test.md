### Feature: Course Enrollment
**Test ID:** TC-CE-001  
**Description:** Verify that the user can successfully enroll in a course.  

**Precondition:**
- User is logged in and on the course details page.

**Steps:**
1. The user selects a course from the list of available courses.
2. The user clicks the "Enroll" button.
3. The user confirms enrollment in the popup dialog.

**Expected Result:**
- The user should be successfully enrolled in the course.
- The user should receive a confirmation message and see the course in their enrolled courses list.

**Status:** Pending/Pass/Fail  




### Feature: Quiz Attempt
**Test ID:** TC-QA-001  
**Description:** Verify that the user can successfully attempt a quiz.  

**Precondition:**
- User is logged in and has enrolled in the course containing the quiz.
- User is on the quiz details page.

**Steps:**
1. The user starts the quiz by clicking the "Start Quiz" button.
2. The user answers all the quiz questions.
3. The user submits the quiz.

**Expected Result:**
- The quiz should be submitted successfully.
- The user should see their score and detailed feedback for each question.

**Status:** Pending/Pass/Fail 

#### Chai.js Code
```javascript
const chai = require('chai');
const expect = chai.expect;
const coursePage = require('../pages/coursePage');

describe('Course Enrollment', function() {
  it('should enroll in a course successfully', function() {
    coursePage.open();
    coursePage.selectCourse('Mathematics for Beginners');
    coursePage.clickEnroll();
    coursePage.confirmEnrollment();
    expect(coursePage.getConfirmationMessage()).to.equal('Enrollment successful');
    expect(coursePage.isCourseInEnrolledList('Mathematics for Beginners')).to.be.true;
  });
});
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -



  

#### Chai.js Code
```javascript
const chai = require('chai');
const expect = chai.expect;
const quizPage = require('../pages/quizPage');

describe('Quiz Attempt', function() {
  it('should allow the user to attempt and submit the quiz successfully', function() {
    quizPage.open();
    quizPage.startQuiz();
    quizPage.answerQuestion(1, 'Option A');
    quizPage.answerQuestion(2, 'Option B');
    quizPage.submitQuiz();
    expect(quizPage.getSubmissionMessage()).to.equal('Quiz submitted successfully');
    expect(quizPage.getScore()).to.be.a('number');
  });
});
