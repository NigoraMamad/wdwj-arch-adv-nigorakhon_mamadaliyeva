# Database Layer Design
## Gym management system 

### Entities 
  1. User(manager)
  2. Member
  3. Membership Type
  4. Instructor
  5. Workout Plan
  6. Workout
  7. Payment
  
### Relationships between the entities.
1. User manages the member information (1 to many relationship).
2. User manages the gym instructor information (1 to many relationship).
3. User encodes type of membership application (1 to many relationship).
4. User processes the payment made by the customer (1 to many relationship).
5. Member belongs to a specific type of membership plan (1 to 1 relationship).
6. Member makes payment for the membership and other fees (1 to many relationship).
7. Member can only enroll to a specific workout plan (1 to 1 relationship).
8. Instructor teaches or guides a specific workout plan (1 to 1 relationship).
9. Workout plan includes multiple types of workouts (1 to many relationship).
    
### Cardinality and ordinality of the relationships.
1.Gym Manager to Membership Type: 1:M (O) - One gym manager can manage many (or zero) membership types.
Membership Type to Gym Manager: M:1 (M) - Many membership types are managed by one gym manager.

2.Gym Manager to Instructor: 1:M (O) - One gym manager can encode many (or zero) instructors.
Instructor to Gym Manager: M:1 (M) - Many instructors are encoded by one gym manager.

3.Member to Membership Type: M:1 (M) - Many members belong to one membership type.
Membership Type to Member: 1:M (O) - One membership type can have many (or zero) members.

4.Member to Payment: 1:M (O) - One member can make many (or zero) payments.
Payment to Member: M:1 (M) - Many payments are made by one member.

5.Instructor to Payment: 1:M (O) - One instructor can process many (or zero) payments.
Payment to Instructor: M:1 (M) - Many payments are processed by one instructor.

6.Member to Workout Plan: 1:M (O) - One member can enroll in many (or zero) workout plans.
Workout Plan to Member: M:1 (O) - One workout plan can have many (or zero) members.

7.Instructor to Workout Plan: 1:M (O) - One instructor can teach many (or zero) workout plans.
Workout Plan to Instructor: M:1 (M) - Many workout plans are teached by one instructor.

8.Workout Plan to Workout: 1:M (M) - One workout plan must have many workouts.
Workout to Workout Plan: M:1 (M) - Many workouts belongs to one workout plan.
### Attributes for the entities (the key, weak key, derived, multivalued attributes).
1. Primary key given as PK
2. Foreign key as fk
