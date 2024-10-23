# Tennis Club Scheduler

This project is a web app for organizing and scheduling tennis matches for a tennis club. The app is designed to help club organizers easily manage match schedules, assign players, and store all match data in Google Sheets for easy access. The interface for organizers is built using **Streamlit**, and match data is stored in **Google Sheets**.

## Features

- Organizers can input match details including date, time, court number, and player assignments.
- Match data is stored in a **Google Sheet** for easy management and access.
- Organizers can view all upcoming matches in a table format for an overview of the schedule.
- Designed with simplicity in mind, making it easy for organizers to input and manage match data.

## Getting Started

### Prerequisites

- **Python 3.7+** installed on your system.
- **Google Cloud Account** to enable Google Sheets API and create credentials.

### Installation

1. Clone this repository:
   ```bash
   git clone <repository-url>
   cd tennis_club_scheduler
   ```

2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   # Activate the virtual environment:
   # On Windows
   venv\Scripts\activate
   # On MacOS/Linux
   source venv/bin/activate
   ```

3. Install the dependencies:
   ```bash
   pip install streamlit gspread oauth2client pandas
   ```

4. Enable **Google Sheets API** in your Google Cloud Console.
   - Create a service account and download the JSON credentials file.
   - Rename the credentials file to `google_credentials.json` and place it in the root of your project folder.

5. Share your Google Sheet with the service account email (found in the `google_credentials.json` file, usually ending in `@.iam.gserviceaccount.com`).

### Running the Application

1. Open a terminal in the project folder and run the following command to start the Streamlit app:
   ```bash
   streamlit run organizer_interface.py
   ```

2. Open your web browser and go to the URL provided by Streamlit (usually `http://localhost:8501`).

## Usage

- Use the form on the left side to enter match details (e.g., date, time, court number, and players).
- Click the **Add Match** button to add the match details to the Google Sheet.
- View the table below the form to see all scheduled upcoming matches.

## Google Sheet Setup

- Create a Google Sheet named **Tennis Club Schedule**.
- Ensure the following headers are present in the Google Sheet:
  - `Match Date`, `Match Time`, `Court Number`, `Player 1`, `Player 2`, `Player 3`, `Player 4`.

## Project Structure

- `organizer_interface.py` - The main Streamlit app script.
- `google_credentials.json` - Google Sheets API credentials file.

## Deployment

If you want to make this app accessible to organizers from anywhere, you can deploy it using **Streamlit Cloud** or **Heroku**.

## Contributing

Feel free to fork this repository and submit pull requests if you have improvements or new features you'd like to add.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Thanks to the **Streamlit** team for making data apps easy to build.
- Special thanks to **Google** for providing accessible API services to integrate spreadsheets.

## Contact

For any questions or suggestions, feel free to reach out via GitHub or emai
