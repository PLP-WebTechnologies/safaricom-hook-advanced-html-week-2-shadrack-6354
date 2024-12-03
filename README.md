### Assignment: Building a Multimedia Webpage and a Registration Form  

#### Objective: 
The goal of this assignment is to create a multimedia-rich webpage featuring audio and video elements and design a simple registration form with built-in HTML validation.  

---

### Part 1: Multimedia Webpage 
Create an HTML webpage that includes the following:  
1. **Audio Element**:  
   - Add an audio file using the `<audio>` tag.  
   - Provide controls to play, pause, and adjust the volume.  
   - Use at least one source format (e.g., `.mp3` or `.ogg`).  

2. **Video Element**:  
   - Add a video file using the `<video>` tag.  
   - Provide controls to play, pause, and adjust the volume.  
   - Include at least two source formats for compatibility (e.g., `.mp4` and `.webm`).  
   - Add a poster image that displays before the video plays.  

**Example Output:**  
A webpage where users can play an audio track and watch a video.  
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Audio and Video</title>
</head>
<body>
    <h1>Audio and Video Elements</h1>

    <!-- Audio -->
    <section>
        <h2>Audio Player</h2>
        <audio controls>
            <source src="audio-file.mp3" type="audio/mp3">
            <source src="audio-file.ogg" type="audio/ogg">
            Your browser does not support the audio element.
        </audio>
    </section>

    <!-- Video -->
    <section>
        <h2>Video Player</h2>
        <video controls poster="video-poster.jpg">
            <source src="video-file.mp4" type="video/mp4">
            <source src="video-file.webm" type="video/webm">
            Your browser does not support the video element.
        </video>
    </section>

</body>
</html>

---

### **Part 2: Registration Form **  
Design a user registration form with the following requirements:  

1. **Form Elements**:  
   - Full Name (Text input)  
   - Email Address (Input of type `email`)  
   - Password (Input of type `password`)  
   - Age (Input of type `number`, with a minimum value of 18)  
   - Gender (Radio buttons for Male, Female, Other)  
   - Terms and Conditions (Checkbox to agree before submitting)  

2. **Validation**:  
   - Use HTML5 validation attributes such as `required`, `min`, `maxlength`, etc.  
   - Ensure the email field has proper validation for email format.  
   - Make the password field require at least 8 characters.  

3. **Submit Button**:  
   - Include a "Register" button to submit the form.  

**Example Output:**  
A user-friendly registration form that prevents submission if required fields are not filled correctly.  
<!DOCTYPE html>
<html lang="en">
<head>
    <title>User Registration Form</title>
</head>
<body>
    <h1>User Registration Form</h1>

    <form action="/submit" method="POST">
        <!-- Full Name -->
        <label for="full-name">Full Name:</label>
        <input type="text" id="full-name" name="full-name" required maxlength="100" placeholder="Enter your full name"><br><br>

        <!-- Email Address -->
        <label for="email">Email Address:</label>
        <input type="email" id="email" name="email" required placeholder="Enter your email" /><br><br>

        <!-- Password -->
        <label for="password">Password:</label>
        <input type="password" id="password" name="password" required minlength="8" placeholder="Enter your password" /><br><br>

        <!-- Age -->
        <label for="age">Age:</label>
        <input type="number" id="age" name="age" required min="18" placeholder="Enter your age" /><br><br>

        <!-- Gender -->
        <label>Gender:</label>
        <input type="radio" id="male" name="gender" value="male" required>
        <label for="male">Male</label>
        <input type="radio" id="female" name="gender" value="female">
        <label for="female">Female</label>
        <input type="radio" id="other" name="gender" value="other">
        <label for="other">Other</label><br><br>

        <!-- Terms and Conditions -->
        <label>
            <input type="checkbox" id="terms" name="terms" required>
            I agree to the <a href="#">Terms and Conditions</a>
        </label><br><br>

        <!-- Submit Button -->
        <button type="submit">Register</button>
    </form>

</body>
</html>
---
