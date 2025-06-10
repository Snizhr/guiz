# quiz_app.py

questions = [
    {
        "question": "What is the capital of Pakistan?",
        "options": ["A. Lahore", "B. Quetta", "C. Rawalpindi", "D. Islamabad"],
        "answer": "D"
    },
    {
        "question": "Which language is used to write COMPILER?",
        "options": ["A. Python", "B. Java", "C. C++", "D. Ruby"],
        "answer": "C"
    },
    {
        "question": "What does CPU stand for?",
        "options": ["A. Central Process Unit", "B. Computer Personal Unit", "C. Central Processing Unit", "D. Control Panel Unit"],
        "answer": "C"
    },
    {
        "question": "Jannat ky patty is wrutten by ?",
        "options": ["A.Umerah Ahmed ", "B. Charles Dickens", "C. Nemrah Ahmed", "D. Jane Austen"],
        "answer": "C"
    }
]

def run_quiz(questions):
    score = 0
    for i, q in enumerate(questions, 1):
        print(f"\nQuestion {i}: {q['question']}")
        for option in q["options"]:
            print(option)
        answer = input("Enter your answer (A/B/C/D): ").strip().upper()
        if answer == q["answer"]:
            print("Correct!")
            score += 1
        else:
            print(f"Wrong! The correct answer was {q['answer']}.")
    
    print("\n=== QUIZ COMPLETED ===")
    print(f"Your score: {score} out of {len(questions)}")

if __name__ == "__main__":
    run_quiz(questions)


