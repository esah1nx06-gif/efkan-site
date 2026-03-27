# efkan-site
site
from flask import Flask
import os

app = Flask(__name__)

@app.route("/")
def home():
    return """
    <h1 style='color:gold;'>EFKAN ŞAHİN</h1>
    <p>Lüks. Güç. Karizma.</p>
    <style>
        body {background:black; color:white; text-align:center; margin-top:100px;}
    </style>
    """

if __name__ == "__main__":
    app.run(host="0.0.0.0", port=int(os.environ.get("PORT", 5000)))
