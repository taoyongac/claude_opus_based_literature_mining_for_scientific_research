# claude_opus_based_literature_mining_for_scientific_research

Introduction:
This document outlines a process for conducting scientific research using Claude Opus, a large language model developed by Anthropic. The process involves mining relevant literature through Google searches, processing the collected material with Claude Opus, and synthesizing the information to answer research questions and draw conclusions.
The described workflow consists of three main steps:

Collecting research material by fetching Google search results using a Flask service. The service requires a Google API key and CSE ID, and the collected results are saved as text files for further processing.
Inputting the collected research material into Claude Opus and prompting the model to thoroughly review the content and provide a well-structured, academically rigorous summary that addresses the research question at hand.
Utilizing Claude Opus's capabilities as an expert research assistant to identify relevant quotes from the research material that support the conclusions drawn in step two. The model then incorporates these quotes into the conclusions by referencing them using bracketed numbers.

This process leverages the power of large language models to efficiently gather, analyze, and synthesize information from a wide range of sources, enabling researchers to draw well-supported conclusions and advance their scientific understanding of the topic under investigation.

##########step one:
Collecting material for Claude Opus by fetching 10 pages of Google search results

1. This is a Flask service. To use it, you need to insert your Google API key and CSE ID into the code. Save the file code as app.py；
2. then run python app.py in Visual Studio Code. Open your browser and navigate to 127.0.0.1:5000. 
3. Enter your search keyword, and you'll get the search results. Copy these results into Claude Opus for further use.

More notes:
This service fetches only the first 10 pages of Google search results. If you need more, you'll have to modify the code accordingly.
Considering Claude Opus's input limitation of 200K tokens, the code automatically splits the results into multiple files if they exceed 156K tokens. 
When installing Flask, you might encounter an error prompting you to install the required packages. Additionally, create a downloads folder in the same directory as app.py to store temporary text files containing the search results.



##########Step Two:
copy text from step 1 into claude opus
Prompt: Based on the research materials provided above, answer the following question:"Your question".
Make every effort to thoroughly review the entire body of research material and ensure that no points from the articles are overlooked. Please organize your summary in an academically rigorous, logically coherent manner.
Use academic language, maintain clear structure, and ensure logical organization of your summary. Utilize original text from the materials whenever possible, and employ professional terminology in English.

##########Step Three:
copy text from step 1 into claude opus
Prompt: You are an expert research assistant. First, find the quotes from the attached document that are most relevant to the following conclusions, and then print them in numbered order. Quotes should be relatively short. If there are no relevant quotes, write "No relevant quotes" instead. Then, incorporate quotes into the conclusions by making references to quotes relevant to each section of the conclusion solely by adding their bracketed numbers at the end of relevant sentences.
"Place the conclusions obtained in Step Two here."


More notes:
1. Literature mining with claude opus is far more better than with gpt4. 
2. Consider running multiple iterations of this pipeline rather than just one if your inquiry is particularly significant. For instance, in section 2, present a broader range of questions individually: Does the material mention any new hypotheses or mechanisms? What unresolved questions and future research directions are highlighted? What implications do the material's conclusions hold for research in the field, and what limitations might exist?
3. Delve deeply into the details derived from steps 2 and 3, and pose new inquiries focused on specific topics using the input file from step 1 once more.
