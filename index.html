<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Python 101</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&display=swap" rel="stylesheet">
    <!-- Chosen Palette: Calm Neutrals -->
    <!-- Application Structure Plan: A multi-section single-page application with a persistent sidebar navigation. This non-linear structure allows users to freely explore different Python concepts at their own pace, which is more effective for learning than a static, linear document. The sections are logically grouped into: Welcome, Core Concepts (with sub-navigation), an interactive Code Playground, and Resources. The key interaction is the Code Playground, which simulates the execution of a Python script to provide immediate feedback and reinforce learning. This design prioritizes user engagement and self-directed exploration. -->
    <!-- Visualization & Content Choices: 
        - Report Info: "Why Python is Popular" list -> Goal: Inform/Organize -> Viz: Styled list with icons (Unicode) -> Interaction: Hover effects -> Justification: More visually engaging than a standard list.
        - Report Info: All code snippets -> Goal: Inform/Allow Practice -> Viz: Styled <pre><code> blocks -> Interaction: "Copy to Clipboard" button -> Justification: Facilitates easy use of code examples.
        - Report Info: Data Structures (List, Tuple, Dict) -> Goal: Compare/Inform -> Viz: Three-column layout -> Interaction: Clear side-by-side visual comparison -> Justification: Helps beginners quickly grasp the key differences.
        - Report Info: Final "Putting It Together" example -> Goal: Synthesize/Engage -> Viz: Interactive Code Playground with code, output, and run button -> Interaction: A "Run" button that simulates the script's I/O -> Justification: Transforms a static example into an active, hands-on learning experience.
        - Charts: No quantitative data is present in the source report, so no charts (Chart.js/Plotly) are used. The focus is on conceptual and code-based learning. -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f7f3f0;
            color: #4a4a4a;
        }
        .nav-link {
            transition: all 0.2s ease-in-out;
        }
        .nav-link.active {
            background-color: #e6dfd9;
            color: #8d6e63;
            font-weight: 700;
        }
        .nav-link:hover {
            background-color: #efebe9;
        }
        .content-section {
            display: none;
        }
        .content-section.active {
            display: block;
            animation: fadeIn 0.5s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .code-block {
            background-color: #2d2d2d;
            color: #f8f8f2;
            border-radius: 0.5rem;
            padding: 1rem;
            position: relative;
            overflow-x: auto;
        }
        .code-block button {
            position: absolute;
            top: 0.5rem;
            right: 0.5rem;
            background-color: #444;
            color: white;
            border: none;
            padding: 0.25rem 0.5rem;
            border-radius: 0.25rem;
            cursor: pointer;
            font-size: 0.8rem;
            opacity: 0.7;
            transition: opacity 0.2s;
        }
        .code-block button:hover {
            opacity: 1;
        }
        .code-block code {
            font-family: 'Courier New', Courier, monospace;
        }
        .output-area {
            background-color: #1e1e1e;
            color: #d4d4d4;
            font-family: 'Courier New', Courier, monospace;
            border-radius: 0.5rem;
            padding: 1rem;
            min-height: 150px;
            white-space: pre-wrap;
        }
        .btn-primary {
            background-color: #8d6e63;
            color: white;
            transition: background-color 0.3s;
        }
        .btn-primary:hover {
            background-color: #a1887f;
        }

        /* Modal Styles */
        .modal {
            display: none; /* Hidden by default */
            position: fixed; /* Stay in place */
            z-index: 1000; /* Sit on top */
            left: 0;
            top: 0;
            width: 100%; /* Full width */
            height: 100%; /* Full height */
            overflow: auto; /* Enable scroll if needed */
            background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
            backdrop-filter: blur(5px);
            -webkit-backdrop-filter: blur(5px);
        }

        .modal-content {
            background-color: #fefefe;
            margin: 10% auto; /* 10% from the top and centered */
            padding: 2rem;
            border-radius: 0.75rem;
            width: 80%; /* Could be more responsive */
            max-width: 700px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            position: relative;
            animation: slideIn 0.3s ease-out;
        }

        @keyframes slideIn {
            from { transform: translateY(-50px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }

        .close-button {
            color: #aaa;
            position: absolute;
            top: 1rem;
            right: 1rem;
            font-size: 1.5rem;
            font-weight: bold;
            cursor: pointer;
        }

        .close-button:hover,
        .close-button:focus {
            color: #000;
            text-decoration: none;
            cursor: pointer;
        }

        .quiz-feedback {
            margin-top: 1rem;
            padding: 0.75rem;
            border-radius: 0.5rem;
            font-weight: bold;
        }
        .quiz-feedback.correct {
            background-color: #d4edda; /* Light green */
            color: #155724; /* Dark green */
        }
        .quiz-feedback.incorrect {
            background-color: #f8d7da; /* Light red */
            color: #721c24; /* Dark red */
        }
    </style>
</head>
<body class="antialiased">

    <div class="flex flex-col md:flex-row min-h-screen">
        <!-- Sidebar Navigation -->
        <aside class="w-full md:w-64 bg-[#efebe9] p-4 md:p-6 border-r border-gray-200 shrink-0">
            <h1 class="text-2xl font-bold text-[#5d4037] mb-6">Python 101 🐍</h1>
            <nav class="space-y-2">
                <a href="#welcome" class="nav-link block p-3 rounded-lg active">Welcome</a>
                <div>
                    <h2 class="text-sm font-semibold text-gray-500 uppercase mt-4 mb-2 px-3">Core Concepts</h2>
                    <a href="#variables" class="nav-link block p-3 rounded-lg">Variables & Data Types</a>
                    <a href="#operators" class="nav-link block p-3 rounded-lg">Operators</a>
                    <a href="#control-flow" class="nav-link block p-3 rounded-lg">Control Flow</a>
                    <a href="#data-structures" class="nav-link block p-3 rounded-lg">Data Structures</a>
                    <a href="#functions" class="nav-link block p-3 rounded-lg">Functions</a>
                </div>
                <a href="#playground" class="nav-link block p-3 rounded-lg">Code Playground</a>
                <a href="#resources" class="nav-link block p-3 rounded-lg">Next Steps</a>
            </nav>
        </aside>

        <!-- Main Content -->
        <main class="flex-1 p-6 md:p-10 lg:p-12 overflow-y-auto">

            <!-- Welcome Section -->
            <section id="welcome" class="content-section active">
                <h2 class="text-4xl font-bold text-[#5d4037] mb-4">Welcome to Interactive Python 101</h2>
                <p class="text-lg text-gray-600 mb-6">This interactive guide is designed to introduce you to the fundamental concepts of Python. Navigate through the topics using the sidebar to learn at your own pace. Python is a high-level, interpreted, general-purpose programming language known for its emphasis on code readability.</p>
                
                <div class="bg-white p-6 rounded-xl shadow-sm">
                    <h3 class="text-2xl font-bold text-[#5d4037] mb-4">Why is Python so Popular?</h3>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <div class="flex items-start space-x-4">
                            <span class="text-3xl">✨</span>
                            <div>
                                <h4 class="font-bold text-lg">Simplicity & Readability</h4>
                                <p class="text-gray-600">Its clean syntax resembles natural language, making it easy to learn and understand.</p>
                            </div>
                        </div>
                        <div class="flex items-start space-x-4">
                            <span class="text-3xl">📚</span>
                            <div>
                                <h4 class="font-bold text-lg">Vast Ecosystem of Libraries</h4>
                                <p class="text-gray-600">Access extensive libraries for AI, data science, web development, and more (e.g., NumPy, TensorFlow).</p>
                            </div>
                        </div>
                        <div class="flex items-start space-x-4">
                            <span class="text-3xl">🤸</span>
                            <div>
                                <h4 class="font-bold text-lg">Flexibility</h4>
                                <p class="text-gray-600">Supports multiple programming paradigms like object-oriented and functional programming.</p>
                            </div>
                        </div>
                        <div class="flex items-start space-x-4">
                            <span class="text-3xl">🌐</span>
                            <div>
                                <h4 class="font-bold text-lg">Platform Independence</h4>
                                <p class="text-gray-600">Write code once and run it on Windows, macOS, or Linux without modification.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Variables & Data Types Section -->
            <section id="variables" class="content-section">
                <h2 class="text-4xl font-bold text-[#5d4037] mb-4">Variables & Data Types</h2>
                <p class="text-lg text-gray-600 mb-6">Variables are containers for storing data values. Python is dynamically typed, so you don't need to declare the type of a variable. Here are the basic types:</p>
                <div class="space-y-6">
                    <div>
                        <h3 class="text-xl font-semibold mb-2">Integers (`int`) - Whole numbers.</h3>
                        <div class="code-block"><button onclick="copyCode(this)">Copy</button><code>age = 30</code><button class="explain-code-btn">✨ Explain Code</button></div>
                    </div>
                    <div>
                        <h3 class="text-xl font-semibold mb-2">Floats (`float`) - Numbers with a decimal point.</h3>
                        <div class="code-block"><button onclick="copyCode(this)">Copy</button><code>price = 19.99</code><button class="explain-code-btn">✨ Explain Code</button></div>
                    </div>
                    <div>
                        <h3 class="text-xl font-semibold mb-2">Strings (`str`) - Sequences of characters.</h3>
                        <div class="code-block"><button onclick="copyCode(this)">Copy</button><code>name = "Alice"
message = 'Hello, world!'</code><button class="explain-code-btn">✨ Explain Code</button></div>
                    </div>
                    <div>
                        <h3 class="text-xl font-semibold mb-2">Booleans (`bool`) - Represents `True` or `False`.</h3>
                        <div class="code-block"><button onclick="copyCode(this)">Copy</button><code>is_active = True</code><button class="explain-code-btn">✨ Explain Code</button></div>
                    </div>
                </div>

                <div class="bg-white p-6 rounded-xl shadow-sm mt-8">
                    <h3 class="text-2xl font-bold text-[#5d4037] mb-4">Quiz Practice: Variables & Data Types</h3>
                    <div id="variables-quiz-container">
                        <p id="variables-quiz-question" class="text-lg mb-4"></p>
                        <div id="variables-quiz-options" class="space-y-2"></div>
                        <button class="btn-primary mt-4 py-2 px-4 rounded-lg font-bold" onclick="checkQuizAnswer('variables')">Check Answer</button>
                        <div id="variables-quiz-feedback" class="quiz-feedback hidden"></div>
                    </div>
                </div>
            </section>

            <!-- Operators Section -->
            <section id="operators" class="content-section">
                <h2 class="text-4xl font-bold text-[#5d4037] mb-4">Operators</h2>
                <p class="text-lg text-gray-600 mb-6">Operators are special symbols that perform operations on variables and values.</p>
                <div class="space-y-6">
                    <div>
                        <h3 class="text-xl font-semibold mb-2">Arithmetic Operators</h3>
                        <div class="code-block"><button onclick="copyCode(this)">Copy</button><code>result = 10 + 5    # Addition: 15
power = 2 ** 3     # Exponentiation: 8
remainder = 10 % 3 # Modulus: 1</code><button class="explain-code-btn">✨ Explain Code</button></div>
                    </div>
                    <div>
                        <h3 class="text-xl font-semibold mb-2">Comparison Operators</h3>
                        <div class="code-block"><button onclick="copyCode(this)">Copy</button><code>10 == 10  # Equal: True
5 > 10    # Greater than: False
'a' != 'b' # Not equal: True</code><button class="explain-code-btn">✨ Explain Code</button></div>
                    </div>
                    <div>
                        <h3 class="text-xl font-semibold mb-2">Logical Operators</h3>
                        <div class="code-block"><button onclick="copyCode(this)">Copy</button><code>(5 > 3) and (10 < 20) # and: True
(5 < 3) or (10 < 20)  # or: True
not (5 == 5)          # not: False</code><button class="explain-code-btn">✨ Explain Code</button></div>
                    </div>
                </div>

                <div class="bg-white p-6 rounded-xl shadow-sm mt-8">
                    <h3 class="text-2xl font-bold text-[#5d4037] mb-4">Quiz Practice: Operators</h3>
                    <div id="operators-quiz-container">
                        <p id="operators-quiz-question" class="text-lg mb-4"></p>
                        <div id="operators-quiz-options" class="space-y-2"></div>
                        <button class="btn-primary mt-4 py-2 px-4 rounded-lg font-bold" onclick="checkQuizAnswer('operators')">Check Answer</button>
                        <div id="operators-quiz-feedback" class="quiz-feedback hidden"></div>
                    </div>
                </div>
            </section>

            <!-- Control Flow Section -->
            <section id="control-flow" class="content-section">
                <h2 class="text-4xl font-bold text-[#5d4037] mb-4">Control Flow</h2>
                <p class="text-lg text-gray-600 mb-6">Control flow statements allow you to alter the execution order of your code based on conditions and loops.</p>
                <div class="space-y-8">
                    <div>
                        <h3 class="text-2xl font-semibold mb-2">Conditional Logic: `if`, `elif`, `else`</h3>
                        <p class="mb-4">Execute different blocks of code based on whether a condition is true.</p>
                        <div class="code-block"><button onclick="copyCode(this)">Copy</button><code>temperature = 25

if temperature > 30:
    print("It's hot outside!")
elif temperature > 20:
    print("It's a pleasant day.")
else:
    print("It's a bit chilly.")</code><button class="explain-code-btn">✨ Explain Code</button></div>
                    </div>
                    <div>
                        <h3 class="text-2xl font-semibold mb-2">Iteration: `for` Loops</h3>
                        <p class="mb-4">Iterate over a sequence (like a list or a range of numbers).</p>
                        <div class="code-block"><button onclick="copyCode(this)">Copy</button><code># Loop through a list of fruits
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)</code><button class="explain-code-btn">✨ Explain Code</button></div>
                    </div>
                    <div>
                        <h3 class="text-2xl font-semibold mb-2">Conditional Repetition: `while` Loops</h3>
                        <p class="mb-4">Repeat a block of code as long as a certain condition remains true.</p>
                        <div class="code-block"><button onclick="copyCode(this)">Copy</button><code>count = 0
while count < 3:
    print("Count:", count)
    count += 1</code><button class="explain-code-btn">✨ Explain Code</button></div>
                    </div>
                </div>

                <div class="bg-white p-6 rounded-xl shadow-sm mt-8">
                    <h3 class="text-2xl font-bold text-[#5d4037] mb-4">Quiz Practice: Control Flow</h3>
                    <div id="control-flow-quiz-container">
                        <p id="control-flow-quiz-question" class="text-lg mb-4"></p>
                        <div id="control-flow-quiz-options" class="space-y-2"></div>
                        <button class="btn-primary mt-4 py-2 px-4 rounded-lg font-bold" onclick="checkQuizAnswer('control-flow')">Check Answer</button>
                        <div id="control-flow-quiz-feedback" class="quiz-feedback hidden"></div>
                    </div>
                </div>
            </section>

            <!-- Data Structures Section -->
            <section id="data-structures" class="content-section">
                <h2 class="text-4xl font-bold text-[#5d4037] mb-4">Data Structures</h2>
                <p class="text-lg text-gray-600 mb-6">Python provides several built-in data structures to store collections of data efficiently.</p>
                <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                    <div class="bg-white p-6 rounded-xl shadow-sm">
                        <h3 class="text-2xl font-bold text-[#5d4037] mb-3">Lists `[]`</h3>
                        <p class="mb-4 text-gray-600"><strong class="text-gray-800">Ordered</strong> and <strong class="text-gray-800">mutable</strong> (changeable). Great for collections of items you need to modify.</p>
                        <div class="code-block"><button onclick="copyCode(this)">Copy</button><code>my_list = [1, "hello"]
my_list.append(True)
my_list[0] = "world"
print(my_list)</code><button class="explain-code-btn">✨ Explain Code</button></div>
                    </div>
                    <div class="bg-white p-6 rounded-xl shadow-sm">
                        <h3 class="text-2xl font-bold text-[#5d4037] mb-3">Tuples `()`</h3>
                        <p class="mb-4 text-gray-600"><strong class="text-gray-800">Ordered</strong> and <strong class="text-gray-800">immutable</strong> (unchangeable). Useful for data that should not be altered.</p>
                        <div class="code-block"><button onclick="copyCode(this)">Copy</button><code>my_tuple = (1, "hello")
print(my_tuple[1])
# my_tuple[0] = 5 # Error!</code><button class="explain-code-btn">✨ Explain Code</button></div>
                    </div>
                    <div class="bg-white p-6 rounded-xl shadow-sm">
                        <h3 class="text-2xl font-bold text-[#5d4037] mb-3">Dictionaries `{}`</h3>
                        <p class="mb-4 text-gray-600"><strong class="text-gray-800">Key-Value pairs</strong> and <strong class="text-gray-800">mutable</strong>. Perfect for mapping unique keys to specific values.</p>
                        <div class="code-block"><button onclick="copyCode(this)">Copy</button><code>person = {"name": "Bob"}
person["age"] = 25
print(person["name"])</code><button class="explain-code-btn">✨ Explain Code</button></div>
                    </div>
                </div>

                <div class="bg-white p-6 rounded-xl shadow-sm mt-8">
                    <h3 class="text-2xl font-bold text-[#5d4037] mb-4">Quiz Practice: Data Structures</h3>
                    <div id="data-structures-quiz-container">
                        <p id="data-structures-quiz-question" class="text-lg mb-4"></p>
                        <div id="data-structures-quiz-options" class="space-y-2"></div>
                        <button class="btn-primary mt-4 py-2 px-4 rounded-lg font-bold" onclick="checkQuizAnswer('data-structures')">Check Answer</button>
                        <div id="data-structures-quiz-feedback" class="quiz-feedback hidden"></div>
                    </div>
                </div>
            </section>

            <!-- Functions Section -->
            <section id="functions" class="content-section">
                <h2 class="text-4xl font-bold text-[#5d4037] mb-4">Functions</h2>
                <p class="text-lg text-gray-600 mb-6">Functions are reusable blocks of code that perform a specific action. They help organize your code and make it more modular.</p>
                <div class="space-y-8">
                    <div>
                        <h3 class="text-2xl font-semibold mb-2">Defining and Calling a Function</h3>
                        <p class="mb-4">Use the `def` keyword to define a function. Call it by using its name followed by parentheses.</p>
                        <div class="code-block"><button onclick="copyCode(this)">Copy</button><code># Define a function
def greet(name):
    print(f"Hello, {name}!")

# Call the function
greet("Team")</code><button class="explain-code-btn">✨ Explain Code</button></div>
                    </div>
                    <div>
                        <h3 class="text-2xl font-semibold mb-2">Functions with Return Values</h3>
                        <p class="mb-4">Use the `return` statement to send a value back from the function.</p>
                        <div class="code-block"><button onclick="copyCode(this)">Copy</button><code>def add_numbers(a, b):
    return a + b

sum_result = add_numbers(10, 7)
print(f"The sum is: {sum_result}")</code><button class="explain-code-btn">✨ Explain Code</button></div>
                    </div>
                </div>

                <div class="bg-white p-6 rounded-xl shadow-sm mt-8">
                    <h3 class="text-2xl font-bold text-[#5d4037] mb-4">Quiz Practice: Functions</h3>
                    <div id="functions-quiz-container">
                        <p id="functions-quiz-question" class="text-lg mb-4"></p>
                        <div id="functions-quiz-options" class="space-y-2"></div>
                        <button class="btn-primary mt-4 py-2 px-4 rounded-lg font-bold" onclick="checkQuizAnswer('functions')">Check Answer</button>
                        <div id="functions-quiz-feedback" class="quiz-feedback hidden"></div>
                    </div>
                </div>
            </section>

            <!-- Code Playground Section -->
            <section id="playground" class="content-section">
                <h2 class="text-4xl font-bold text-[#5d4037] mb-4">Code Playground</h2>
                <p class="text-lg text-gray-600 mb-6">Let's put it all together! This example calculates a user's approximate age in days. Click "Run Simulation" to see it in action. You will be prompted for input.</p>
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                    <div>
                        <h3 class="text-xl font-semibold mb-2">Python Code</h3>
                        <div class="code-block h-full"><button onclick="copyCode(this)">Copy</button><code>def calculate_days_old(years):
    # Ignores leap years for simplicity
    return years * 365

def main():
    print("--- Age in Days Calculator ---")
    try:
        age_str = input("Please enter your age in years: ")
        age_years = int(age_str)

        if age_years < 0:
            print("Age cannot be negative.")
        else:
            days = calculate_days_old(age_years)
            print(f"You are approx. {days} days old!")
    except ValueError:
        print("Invalid input. Please enter a number.")
    finally:
        print("--- Thank you for using the calculator! ---")

# Run the main function
main()</code><button class="explain-code-btn">✨ Explain Code</button></div>
                    </div>
                    <div>
                        <h3 class="text-xl font-semibold mb-2">Simulated Output</h3>
                        <div id="outputArea" class="output-area"></div>
                        <button id="runButton" class="btn-primary w-full mt-4 py-3 rounded-lg font-bold">Run Simulation</button>
                    </div>
                </div>
            </section>

            <!-- Resources Section -->
            <section id="resources" class="content-section">
                <h2 class="text-4xl font-bold text-[#5d4037] mb-4">Next Steps & Resources</h2>
                <p class="text-lg text-gray-600 mb-6">You've completed the basics! The best way to learn is by practicing. Here are some excellent resources to continue your journey:</p>
                
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mb-8">
                    <a href="https://realpython.com/" target="_blank" class="block bg-white p-6 rounded-xl shadow-sm hover:shadow-md transition-shadow">
                        <h3 class="font-bold text-lg text-[#5d4037]">Real Python</h3>
                        <p class="text-gray-600">In-depth tutorials and articles.</p>
                    </a>
                    <a href="https://www.w3schools.com/python/" target="_blank" class="block bg-white p-6 rounded-xl shadow-sm hover:shadow-md transition-shadow">
                        <h3 class="font-bold text-lg text-[#5d4037]">W3Schools</h3>
                        <p class="text-gray-600">Interactive examples and references.</p>
                    </a>
                    <a href="https://docs.python.org/3/tutorial/index.html" target="_blank" class="block bg-white p-6 rounded-xl shadow-sm hover:shadow-md transition-shadow">
                        <h3 class="font-bold text-lg text-[#5d4037]">Official Python Docs</h3>
                        <p class="text-gray-600">The official Python tutorial.</p>
                    </a>
                </div>

                <div class="bg-white p-6 rounded-xl shadow-sm">
                    <h3 class="text-2xl font-bold text-[#5d4037] mb-4">✨ Python Concept Clarifier</h3>
                    <p class="text-gray-600 mb-4">Enter a Python concept or keyword below, and I'll try to provide a simple explanation using AI.</p>
                    <input type="text" id="conceptInput" placeholder="e.g., 'mutable', 'decorator', 'class'" class="w-full p-3 border border-gray-300 rounded-lg mb-4 focus:outline-none focus:ring-2 focus:ring-[#8d6e63]">
                    <button id="clarifyConceptButton" class="btn-primary w-full py-3 rounded-lg font-bold">✨ Clarify Concept</button>
                    <div id="conceptOutput" class="output-area mt-4 text-gray-700 bg-gray-50 border border-gray-200" style="min-height: 80px;"></div>
                </div>

                <h3 class="text-2xl font-semibold mt-10 mb-4">Advanced Topics to Explore</h3>
                <ul class="list-disc list-inside text-gray-700 space-y-2">
                    <li>Object-Oriented Programming (OOP)</li>
                    <li>File Input/Output</li>
                    <li>Error Handling with `try...except`</li>
                    <li>Modules & Packages</li>
                    <li>Working with libraries like NumPy and Pandas for data science.</li>
                </ul>
            </section>
        </main>
    </div>

    <!-- Explanation Modal -->
    <div id="explanationModal" class="modal">
        <div class="modal-content">
            <span class="close-button" id="closeModalButton">&times;</span>
            <h3 class="text-2xl font-bold text-[#5d4037] mb-4">Code Explanation</h3>
            <div id="modalExplanationContent" class="text-gray-700 pb-4"></div>
            <button id="closeModalButtonBottom" class="btn-primary px-6 py-2 rounded-lg font-bold float-right">Close</button>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const navLinks = document.querySelectorAll('.nav-link');
            const contentSections = document.querySelectorAll('.content-section');
            const explainCodeButtons = document.querySelectorAll('.explain-code-btn');
            const explanationModal = document.getElementById('explanationModal');
            const closeModalButton = document.getElementById('closeModalButton');
            const closeModalButtonBottom = document.getElementById('closeModalButtonBottom');
            const modalExplanationContent = document.getElementById('modalExplanationContent');
            const conceptInput = document.getElementById('conceptInput');
            const clarifyConceptButton = document.getElementById('clarifyConceptButton');
            const conceptOutput = document.getElementById('conceptOutput');

            // Quiz Data
            const quizzes = {
                'variables': {
                    question: "What will be the data type of `temperature` after this code: `temperature = 98.6`?",
                    options: ["int", "float", "str", "bool"],
                    answer: "float"
                },
                'operators': {
                    question: "What is the result of the Python expression: `15 // 4`?",
                    options: ["3.75", "3", "4", "Error"],
                    answer: "3"
                },
                'control-flow': {
                    question: "Given `x = 10`, what will this code print: `if x > 15: print('A') elif x > 5: print('B') else: print('C')`?",
                    options: ["A", "B", "C", "Nothing"],
                    answer: "B"
                },
                'data-structures': {
                    question: "Which of the following Python data structures is immutable (cannot be changed after creation)?",
                    options: ["list", "tuple", "dictionary", "set"],
                    answer: "tuple"
                },
                'functions': {
                    question: "What will be printed when `greet('World')` is called, given: `def greet(name): print(f'Hello, {name}!')`?",
                    options: ["greet('World')", "Hello, name!", "Hello, World!", "Error"],
                    answer: "Hello, World!"
                }
            };

            function showSection(hash) {
                const targetId = hash ? hash.substring(1) : 'welcome';
                
                contentSections.forEach(section => {
                    if (section.id === targetId) {
                        section.classList.add('active');
                    } else {
                        section.classList.remove('active');
                    }
                });

                navLinks.forEach(link => {
                    if (link.getAttribute('href') === `#${targetId}`) {
                        link.classList.add('active');
                    } else {
                        link.classList.remove('active');
                    }
                });

                // Initialize quiz for the active section
                if (quizzes[targetId]) {
                    renderQuiz(targetId);
                }
            }

            navLinks.forEach(link => {
                link.addEventListener('click', (event) => {
                    event.preventDefault();
                    const targetId = link.getAttribute('href');
                    window.location.hash = targetId;
                });
            });
            
            window.addEventListener('hashchange', () => {
                showSection(window.location.hash);
            });

            showSection(window.location.hash);

            const runButton = document.getElementById('runButton');
            const outputArea = document.getElementById('outputArea');

            runButton.addEventListener('click', async () => {
                outputArea.textContent = '';
                runButton.disabled = true;
                runButton.textContent = 'Running...';

                function printToOutput(text) {
                    outputArea.textContent += text + '\n';
                }

                async function inputFromUser(prompt) {
                    printToOutput(prompt);
                    const userInput = window.prompt(prompt);
                    printToOutput('> ' + (userInput || ''));
                    return userInput || '';
                }

                try {
                    printToOutput("--- Age in Days Calculator ---");
                    const age_str = await inputFromUser("Please enter your age in years: ");
                    const age_years = parseInt(age_str, 10);

                    if (isNaN(age_years)) {
                        throw new Error('ValueError');
                    }

                    if (age_years < 0) {
                        printToOutput("Age cannot be negative.");
                    } else {
                        const days = age_years * 365;
                        printToOutput(`You are approx. ${days} days old!`);
                    }
                } catch (e) {
                    printToOutput("Invalid input. Please enter a number.");
                } finally {
                    printToOutput("--- Thank you for using the calculator! ---");
                }
                
                runButton.disabled = false;
                runButton.textContent = 'Run Simulation';
            });

            function copyCode(button) {
                const codeBlock = button.parentElement;
                const code = codeBlock.querySelector('code').innerText;
                
                const textarea = document.createElement('textarea');
                textarea.value = code;
                document.body.appendChild(textarea);
                textarea.select();
                document.execCommand('copy');
                document.body.removeChild(textarea);

                const originalText = button.textContent;
                button.textContent = 'Copied!';
                setTimeout(() => {
                    button.textContent = originalText;
                }, 2000);
            }
            window.copyCode = copyCode; 

            // Gemini API Integration
            async function callGeminiApi(prompt) {
                const maxRetries = 3;
                let retryCount = 0;
                const apiKey = ""; 

                while (retryCount < maxRetries) {
                    try {
                        const chatHistory = [];
                        chatHistory.push({ role: "user", parts: [{ text: prompt }] });
                        const payload = { contents: chatHistory };
                        const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-05-20:generateContent?key=${apiKey}`;
                        
                        const response = await fetch(apiUrl, {
                            method: 'POST',
                            headers: { 'Content-Type': 'application/json' },
                            body: JSON.stringify(payload)
                        });

                        if (!response.ok) {
                            throw new Error(`HTTP error! status: ${response.status}`);
                        }

                        const result = await response.json();
                        if (result.candidates && result.candidates.length > 0 &&
                            result.candidates[0].content && result.candidates[0].content.parts &&
                            result.candidates[0].content.parts.length > 0) {
                            return result.candidates[0].content.parts[0].text;
                        } else {
                            throw new Error("Invalid API response structure.");
                        }
                    } catch (error) {
                        retryCount++;
                        if (retryCount < maxRetries) {
                            const delay = Math.pow(2, retryCount) * 1000; 
                            await new Promise(res => setTimeout(res, delay));
                        } else {
                            console.error("Gemini API call failed after multiple retries:", error);
                            return "Error: Could not retrieve explanation. Please try again.";
                        }
                    }
                }
            }

            // Code Explanation Feature
            explainCodeButtons.forEach(button => {
                button.addEventListener('click', async () => {
                    const codeBlock = button.parentElement;
                    const code = codeBlock.querySelector('code').innerText;
                    
                    showModal('Loading explanation...');

                    const prompt = `Explain the following Python code snippet in a simple, beginner-friendly way:\n\n\`\`\`python\n${code}\n\`\`\``;
                    const explanation = await callGeminiApi(prompt);
                    updateModalContent(explanation);
                });
            });

            closeModalButton.addEventListener('click', () => {
                explanationModal.style.display = 'none';
            });
            closeModalButtonBottom.addEventListener('click', () => {
                explanationModal.style.display = 'none';
            });
            window.addEventListener('click', (event) => {
                if (event.target == explanationModal) {
                    explanationModal.style.display = 'none';
                }
            });

            function showModal(content) {
                modalExplanationContent.innerHTML = content;
                explanationModal.style.display = 'block';
            }

            function updateModalContent(content) {
                modalExplanationContent.innerHTML = content;
            }

            // Concept Clarifier Feature
            clarifyConceptButton.addEventListener('click', async () => {
                const concept = conceptInput.value.trim();
                if (!concept) {
                    conceptOutput.textContent = "Please enter a concept to clarify.";
                    return;
                }

                conceptOutput.textContent = "Clarifying concept...";
                clarifyConceptButton.disabled = true;

                const prompt = `Explain the Python concept or keyword '${concept}' in a concise and easy-to-understand manner for a beginner.`;
                const explanation = await callGeminiApi(prompt);
                conceptOutput.textContent = explanation;
                clarifyConceptButton.disabled = false;
            });

            // Quiz Functions
            function renderQuiz(sectionId) {
                const quiz = quizzes[sectionId];
                if (!quiz) return;

                const quizQuestionElem = document.getElementById(`${sectionId}-quiz-question`);
                const quizOptionsElem = document.getElementById(`${sectionId}-quiz-options`);
                const quizFeedbackElem = document.getElementById(`${sectionId}-quiz-feedback`);

                quizQuestionElem.textContent = quiz.question;
                quizOptionsElem.innerHTML = ''; // Clear previous options
                quizFeedbackElem.classList.add('hidden'); // Hide feedback

                quiz.options.forEach((option, index) => {
                    const radioId = `${sectionId}-option-${index}`;
                    const div = document.createElement('div');
                    div.innerHTML = `
                        <input type="radio" id="${radioId}" name="${sectionId}-quiz-option" value="${option}" class="mr-2">
                        <label for="${radioId}">${option}</label>
                    `;
                    quizOptionsElem.appendChild(div);
                });
            }

            window.checkQuizAnswer = function(sectionId) {
                const quiz = quizzes[sectionId];
                if (!quiz) return;

                const selectedOption = document.querySelector(`input[name="${sectionId}-quiz-option"]:checked`);
                const quizFeedbackElem = document.getElementById(`${sectionId}-quiz-feedback`);
                
                quizFeedbackElem.classList.remove('hidden', 'correct', 'incorrect');

                if (selectedOption) {
                    if (selectedOption.value === quiz.answer) {
                        quizFeedbackElem.textContent = "🎉 Correct! Great job.";
                        quizFeedbackElem.classList.add('correct');
                    } else {
                        quizFeedbackElem.textContent = `❌ Incorrect. The correct answer was "${quiz.answer}".`;
                        quizFeedbackElem.classList.add('incorrect');
                    }
                } else {
                    quizFeedbackElem.textContent = "Please select an answer.";
                    quizFeedbackElem.classList.add('incorrect');
                }
            };

            // Initial render of quizzes for visible sections (if any are active on load)
            contentSections.forEach(section => {
                if (section.classList.contains('active') && quizzes[section.id]) {
                    renderQuiz(section.id);
                }
            });
        });
    </script>
</body>
</html>
