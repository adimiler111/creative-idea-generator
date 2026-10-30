# Creative Idea Generator

A beginner-friendly Google Colab notebook that suggests **one unusual but practical use** for an everyday object using the OpenAI Responses API and `gpt-6-luna`.

## Run in Google Colab

1. Download `creative_ideas.ipynb` from this folder.
2. Open [Google Colab](https://colab.research.google.com/) and choose **File > Upload notebook**. Select `creative_ideas.ipynb`.
3. Run the SDK installation cell using its play button.
4. Run the next code cell, enter an everyday object, and enter your OpenAI API key in the hidden prompt.
5. Read your idea! Run the second code cell again to try another object.

You need an OpenAI API key and access to `gpt-6-luna`. API usage may incur charges. If a request fails, check your key, model access, billing, and internet connection.

## Keep your key private

- Enter the API key only in the `getpass` prompt. It is hidden while you type.
- Never paste the key into notebook cells, the README, outputs, or GitHub.
- The code keeps the key in runtime memory only, does not print it or write it to a file, and removes its references after the request. It sends the key to OpenAI to authenticate the API request.
- Before downloading or sharing a used notebook, clear all cell outputs and disconnect/delete the Colab runtime. Review the file to ensure it contains no secrets.
- This notebook is supplied with no saved outputs or API keys.

The notebook installs the OpenAI Python SDK and uses `client.responses.create(...)` and `response.output_text`, following the [official OpenAI text generation guide](https://developers.openai.com/api/docs/guides/text?lang=python).

No GitHub commit or push has been made.
