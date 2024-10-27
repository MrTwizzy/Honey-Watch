# HoneyWatch: Visual Network Attack Monitor with Global Threat Tracking

A lightweight web-based honeypot monitoring system that tracks connection attempts and displays them with geolocation data. Built with Flask, this tool provides a simple way to monitor and log potential network reconnaissance activities.

[![Screenshot-2024-10-27-08-29-03-03-40deb401b9ffe8e1df2f1cc5ba480b12.jpg](https://i.postimg.cc/LXSW55BB/Screenshot-2024-10-27-08-29-03-03-40deb401b9ffe8e1df2f1cc5ba480b12.jpg)](https://postimg.cc/XZ2LDVPp)

## Features

- Real-time connection monitoring with web interface
- IP geolocation tracking using ip-api.com
- Country detection with flag indicators
- Timestamp recording for all connections
- Port availability checking
- Clean, responsive web interface
- No database required - in-memory storage

## Requirements

- Python 3.6+
- Flask
- Requests

## Installation

1. Clone the repository:
```bash
git clone https://github.com/MrTwizzy/Honey-Watch.git
cd Honey-Watch
```

2. Install required packages:
```bash
pip install flask requests
```

3. Run the honeypot:
```bash
python honeypot.py
```

4. Enter your desired port number when prompted (e.g., 8080)

## Usage

After starting the application:

1. The web interface will be accessible at `http://your-ip:port`
2. Each connection to the honeypot will be logged with:
   - Timestamp
   - IP address
   - Country name and code
   - Country flag emoji
3. Use the "Refresh Data" button to update the display
4. Monitor the terminal for startup messages and errors

## Web Interface

The interface includes:
- Current monitoring port display
- Connection history table
- Manual refresh button
- Responsive design for various screen sizes

## Technical Details

The honeypot consists of:
- Flask web server
- IP geolocation using ip-api.com
- Socket-based port availability checking
- In-memory storage for connection logs
- Built-in country code to flag emoji mapping

## Security Considerations

This is a basic honeypot implementation intended for educational purposes. For production use, consider:
- Adding authentication
- Implementing persistent storage
- Adding rate limiting
- Using HTTPS
- Implementing proper logging
- Adding input validation

## API Usage

The system uses the following external API:
- ip-api.com for IP geolocation (free tier, no API key required)

## Limitations

- Stores data in memory (cleared on restart)
- No persistent logging
- No authentication mechanism
- Limited to basic connection tracking
- Uses free tier of ip-api.com (limited requests)

## License

This project is open source and available under the MIT License.

## Acknowledgements

- Flask for the web framework
- ip-api.com for geolocation services
- Requests library for API communication

## Disclaimer

This tool is designed for educational and research purposes only. Users are responsible for ensuring compliance with applicable laws and regulations.
