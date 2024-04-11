# Report Bugs

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Email Form Example</title>
</head>
<body>
    <form action="send_email.php" method="post">
        <label for="email">Recipient Email:</label>
        <input type="email" id="email" name="email"><br>
        <label for="subject">Subject:</label>
        <input type="text" id="subject" name="subject"><br>
        <label for="message">Message:</label><br>
        <textarea id="message" name="message" rows="4" cols="50"></textarea><br>
        <button type="submit">Send Email</button>
    </form>
</body>
</html>
