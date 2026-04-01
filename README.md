# Info

## Author Information

- **Name:** Juan Vicente Herrera Ruiz de Alejo
- **GitHub:** [@juanviz](https://github.com/juanviz)
- **Role:** Author and Maintainer
- **Affiliation:** ICAI

## License
This project is licensed under the MIT License - see the [MIT License](https://opensource.org/licenses/MIT) for details.

# Currency Converter

This is a simple Python Flask application that converts an amount from euros to dollars using a web interface.

## Usage
Run the server with:

```sh
python main.py
```

Then open your browser at `http://127.0.0.1:5000/` and use the interface to perform conversions.

## Installation
To run the app, install dependencies with:

```sh
pip install -r requirements.txt
```

## Deployment to Google App Engine
1. Install Google Cloud SDK and authenticate:

```sh
gcloud init
```

2. If not present, create `app.yaml` with contents similar to:

```yaml
runtime: python311
entrypoint: gunicorn -b :$PORT main:app

env_variables:
  PORT: 8080
```

3. Make sure `requirements.txt` includes Flask and gunicorn:

```sh
flask
gunicorn
```

4. Test locally:

```sh
gcloud app browse --local-host=127.0.0.1:8080
```

5. Deploy to App Engine:

```sh
gcloud app deploy --quiet --project=${PROJECT_ID}
```

6. Open the application at the App Engine URL printed by the deploy command.

## License
This project is distributed under the MIT License.
