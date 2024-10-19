import pyttsx3

# Initialize the text-to-speech engine
engine = pyttsx3.init()

# Set the properties for the voice, such as rate (speed), volume, and voice type (male/female)
rate = engine.getProperty('rate')   # Get the current rate of speech
engine.setProperty('rate', 150)     # Setting the rate (lower for a more robotic feel)

volume = engine.getProperty('volume')   # Get the current volume level (between 0.0 and 1.0)
engine.setProperty('volume', 1.0)       # Set the volume level (1.0 for max volume)

# Select a voice (optional: customize with male/female)
voices = engine.getProperty('voices')    # Get the available voices
engine.setProperty('voice', voices[0].id)  # Choose voice [0] for male, [1] for female

# Define the text to be spoken
text = "Hello! I am your AI robot. How can I assist you today?"

# Convert the text to speech
engine.say(text)

# Wait until speaking is done
engine.runAndWait()
