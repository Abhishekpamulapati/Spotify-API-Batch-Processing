🎵 Spotify API Batch Processing
A lightweight and modular batch processing toolkit for Spotify Web API tasks such as authentication, token generation, and paginated data extraction of new releases and albums.
📦 Features
- 🎛️ App setup and credential generation via Spotify Developer Portal
- 🔐 OAuth token handling and credential management
- 🔁 Pagination support for New Releases and Albums endpoints
- 📄 Comprehension instructions included to guide users step-by-step
🚀 Getting Started
1. Set Up Spotify App
Create an application in the Spotify Developer Portal to obtain your credentials:
- Client ID
- Client Secret
- Redirect URI
2. Clone the Repository
git clone https://github.com/<your-username>/<your-repository>.git
cd <your-repository>


3. Configure Environment
Create a .env file using your Spotify app credentials:
SPOTIFY_CLIENT_ID=your_client_id
SPOTIFY_CLIENT_SECRET=your_client_secret
SPOTIFY_REDIRECT_URI=http://127.0.0.1:8000/callback


4. Install Dependencies
pip install -r requirements.txt


📚 Usage
Authenticate & Generate Tokens
Run the script to authenticate and obtain access and refresh tokens. These are cached for reuse during batch API calls.
Paginated API Processing
The project includes modules to paginate through:
- /v1/browse/new-releases
- /v1/albums
Each endpoint supports customizable batch size, filtering logic, and rate limiting adherence.
🧪 Example
from spotify_batch import SpotifyBatchClient

client = SpotifyBatchClient()
new_releases = client.get_new_releases(pages=5)
albums = client.get_albums(ids_list)


📝 Documentation
Refer to the instructions.md file for full walkthrough and examples.
💡 Contributing
Feel free to fork the repo, open issues, or submit pull requests!
