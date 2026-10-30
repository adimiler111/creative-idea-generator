# Creative Idea Generator

A beginner-friendly Google Colab notebook that suggests **exactly three unusual but practical ideas**, displayed as a numbered list (1, 2, 3), for an everyday object using the OpenAI Responses API and `gpt-6-luna`.

## Run in Google Colab

1. Download `creative_ideas.ipynb` from this folder.
2. Open [Google Colab](https://colab.research.google.com/) and choose **File > Upload notebook**. Select `creative_ideas.ipynb`.
3. Run the SDK installation cell using its play button.
4. Run the next code cell and enter your OpenAI API key once in the hidden prompt.
5. Enter an everyday object, such as `paper clip` or `coffee mug`. Read the three numbered ideas.
6. Enter another object at the next prompt. Keep trying objects without restarting the notebook or rerunning the cell.
7. Type `exit` to stop the program. Uppercase `EXIT` also works. To start a new session afterward, run the second code cell again.

You need an OpenAI API key and access to `gpt-6-luna`. API usage may incur charges. If a request fails, check your key, model access, billing, and internet connection.

## Keep your key private

- Enter the API key only in the `getpass` prompt. It is hidden while you type.
- Never paste the key into notebook cells, the README, outputs, or GitHub.
- The code keeps the key in runtime memory only, does not print it or write it to a file, and removes its references when the program stops. It sends the key to OpenAI to authenticate the API request.
- Before downloading or sharing a used notebook, clear all cell outputs and disconnect/delete the Colab runtime. Review the file to ensure it contains no secrets.
- This notebook is supplied with no saved outputs or API keys.

The notebook installs the OpenAI Python SDK and uses `client.responses.create(...)` and `response.output_text`, following the [official OpenAI text generation guide](https://developers.openai.com/api/docs/guides/text?lang=python).

The response format requests exactly three ideas, and the code adds the numbers using a simple loop. Blank input asks you to try again; a failed request shows a short message and lets you enter another object. Each non-empty object entry (except `exit`) makes a new API request.

Tested successfully in Google Colab: generates exactly three numbered ideas per object, accepts multiple objects, and stops when you type `exit`.
