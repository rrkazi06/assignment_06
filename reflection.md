# Reflection

## Instructions

Reflections are a metcognitive activity where you are encouraged to think about your own thinking. It helps you build a strong understanding of your own learning. A good learner not only "knows what they know", but they "know what they don't know", too. Learning to reflect takes practice, but if your goal is to become a self-directed learner where you can teach yourself things, reflection is imperative.

- Now that you've completed the assignment, think about what you did and share your thoughts. What did you learn? What confuses you? Where did you struggle? Where might you need more practice?
- A good reflection is: **specific as possible**,  **uses the terminology of the problem domain** (what was learned in class / through readings), and **is actionable** (you can pursue next steps, or be aided in the pursuit). That last part is what will make you a self-directed learner.
- Flex your recall muscles. You might have to review class notes / assigned readings to write your reflection and get the terminology correct.
- Your reflection is for **you**. Yes I make you write them and I read them, but you are merely practicing to become a better self-directed learner. If you read your reflection 1 week later, does what you wrote advance your learning?

Examples:

- **Poor Reflection:**  "I don't understand loops."   
**Better Reflection:** "I don't undersand how the while loop exits."   
**Best Reflection:** "I struggle writing the proper exit conditions on a while loop." It's actionable: You can practice this, google it, ask Chat GPT to explain it, etc. 
-  **Poor Reflection** "I learned loops."   
**Better Reflection** "I learned how to write while loops and their difference from for loops."   
**Best Reflection** "I learned when to use while vs for loops. While loops are for sentiel-controlled values (waiting for a condition to occur), vs for loops are for iterating over collections of fixed values."

`--- Write your reflection in the file code/reflection.txt ---`

During this assignment, I learned how different parts of a Python data pipeline work together, especially when extracting, transforming, and analyzing data. I became more comfortable working with REST APIs, JSON responses, and pandas. I also learned the importance of understanding the grain of a DataFrame, or what each row represents, before combining tables with pd.merge() or pd.concat().

One of my biggest struggles was debugging errors caused by passing the wrong data between functions. For example, I encountered a KeyError: 'entity_offset' because mention-shaped rows were passed where raw entity rows were expected. I used print(df.columns) to trace the issue and realized the data had already been processed before reaching the function. This helped me understand why it is important to track where variables come from and what structure each function expects. I also struggled with column names changing after merges, such as sentence_id_x and sentence_id_y. I learned to pay closer attention to overlapping columns and join keys instead of assuming all the original columns would remain unchanged.

Another important learning moment involved the weather question. The model was using all 73 mentions because evidence_for returns everything when a question does not name a specific entity. I tried adding a scope check, but an existing test failed, so I reverted the change. This helped me realize that the test expected questions without a named entity to still pass all available evidence to the model. I learned that passing tests does not necessarily mean an application works perfectly in every situation, but that tests also represent intended design decisions that I need to understand before changing the code.

Moving forward, I need more practice tracing data through functions and understanding how merges affect DataFrames. To practice, I will create a three-row DataFrame, predict the output of a pd.merge() using shared join keys on paper, and then run the code to compare the results. I also want to get better at debugging by checking column names and following variables through each step rather than relying on trial and error. This will help me become more confident working independently on Python projects involving data analytics and data science.
