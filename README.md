# crawl_for_claude_opus
Collecting material for Claude Opus by fetching 10 pages of Google search results

1. This is a Flask service. To use it, you need to insert your Google API key and CSE ID into the code. Save the file as app.py；
2. then run python app.py in Visual Studio Code. Open your browser and navigate to 127.0.0.1:5000. 
3. Enter your search keyword, and you'll get the search results. Copy these results into Claude Opus for further use.

More notes:
This service fetches only the first 10 pages of Google search results. If you need more, you'll have to modify the code accordingly.

Considering Claude Opus's input limitation of 200K tokens, the code automatically splits the results into multiple files if they exceed 156K tokens. 

When installing Flask, you might encounter an error prompting you to install the required packages. Additionally, create a downloads folder in the same directory as app.py to store temporary text files containing the search results.
