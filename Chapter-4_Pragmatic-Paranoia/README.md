#### A Pragmatic Paranoia

`You can't write perfect software`

- Often taught to code defensively
- If there's any doubt, we validate all information we're given
- Use assertions to detect bad data
- Check for consistency, put constraints on database columns, and generally feel pretty good about themselves

- Pragmatic Programmers take this one step further
- `They don't trust themselves, either`
- Pragmatic Programmers code in defenese against their town mistakes
- `Design by Contract`: clients and suppliers must agree on rights and responsibilities

- In `Dead Programs Tell No Lies` - we want to ensure that we do no damage while we're working the bugs out
- Try to check things often and terminate the program if things go awry

- `Assertive Programming` describes an easy method of checking along the way - write code that actively verififes your assumptions

- Exceptions, like any other technique, can cause more harm than good if not used properly
- Discuss this later in `When to Use Exceptions`

- As your program gets more dynamic, you'll find yourself juggling system - memory, files, devices, and the like
- In `How to Balance Resoures', suggestions about how to handle these

###### Design by Contract

- A contract defines your rights and responsibilites, as well as those of the other party
- There is an agreement concerning repercussions if either party fails to abide by the contract

- It is a simple yet powerful technique that focuses on documenting (and agreeing to) the rights and responsibilities of software modules to ensure program correctness
- What is a correct program?
- Documenting and verifying that claim is the heart of `Design by Contract`

- Every function and method in a software system does `something`
- Before it starts that `something`, the routine may have some expectations of the state of the system, and it may be able to make a statement about the state of the system when it concludes
    * Preconditions - What must be tru ein order for the routine to be called; the routine's requirements
        - A routine should never get called when its preconditions would be vilated
        - `It is the caller's responsibility to pass good data`
    * Postconditions - What the routine is guaranteed to do; the state of the system when the routine is done
        - The fact that the routine has a postcondition implies that it `will` conclude; infinite loops aren't allowed
    * Class invariants - A class ensures that this condition is always true from the perspective of a caller
        - During internal processing of a routine, the invariant may not hold, but by the time the time the routine exists and control returns to the caller, the invariant must be true

```
If all the routine's preconditions are met by theh caller, the routine shall guarantee that all postconditons and invariants will be true when it completed