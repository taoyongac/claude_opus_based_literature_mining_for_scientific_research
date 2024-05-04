# crawl_for_claude_opus
step one:
Collecting material for Claude Opus by fetching 10 pages of Google search results

1. This is a Flask service. To use it, you need to insert your Google API key and CSE ID into the code. Save the file code as app.py；
2. then run python app.py in Visual Studio Code. Open your browser and navigate to 127.0.0.1:5000. 
3. Enter your search keyword, and you'll get the search results. Copy these results into Claude Opus for further use.

More notes:
This service fetches only the first 10 pages of Google search results. If you need more, you'll have to modify the code accordingly.
Considering Claude Opus's input limitation of 200K tokens, the code automatically splits the results into multiple files if they exceed 156K tokens. 
When installing Flask, you might encounter an error prompting you to install the required packages. Additionally, create a downloads folder in the same directory as app.py to store temporary text files containing the search results.



Step Two:
copy text from step 1 into claude opus
Prompt: Based on the research materials provided above, answer the following question:Your question
Make every effort to thoroughly review the entire body of research material and ensure that no points from the articles are overlooked. Please organize your summary in an academically rigorous, logically coherent manner.
Use academic language, maintain clear structure, and ensure logical organization of your summary. Utilize original text from the materials whenever possible, and employ professional terminology in English.

Step Three:
copy text from step 1 into claude opus
Prompt: You are an expert research assistant. First, find the quotes from the attached document that are most relevant to the following conclusions, and then print them in numbered order. Quotes should be relatively short. If there are no relevant quotes, write "No relevant quotes" instead. Then, incorporate quotes into the conclusions by making references to quotes relevant to each section of the conclusion solely by adding their bracketed numbers at the end of relevant sentences.
"Place the conclusions obtained in Step Two here."
