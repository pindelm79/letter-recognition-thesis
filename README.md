# Letter Recognition

This is a public version of my engineering thesis "Application of neural networks in letter recognition". The goal of this project was to build and train a model (from scratch, using pretty much only NumPy) and a web application that can recognize user-drawn English alphabet letters.

To see it in action, go here: http://pindelm79.github.io/letter-recognition.

## Installation

The model is hosted on Azure, so there is no need for installation.

If you have to, you can download the source code from the Releases tab, set up the environment (using ```poetry.lock``` or ```requirements.txt```) and run 
```bash 
flask run
```
You can then call the API (see Usage) at the given IP and port.

## Usage

To run the website locally, open the file ```index.html``` in your browser.

You can also call the API directly at https://letterrecognitionapi.azurewebsites.net/.

The API accepts a JSON file in the format ```{"image": <base64-encoded image>}```.

It returns a JSON in the format:
```
{
    "predicted": <predicted letter>, 
    "confidence": <confidence for the letter>,
    "all": [
        { "letter": <letter>, "probability": <probability for the letter> },
        ...
    ]
}
```

## License
[MIT](https://choosealicense.com/licenses/mit/)
