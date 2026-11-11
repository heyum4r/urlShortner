## IMP
- The frontend’s check saves the user a trip to the server, but the backend’s check is the one the system actually relies on.

- Database:- an organized collection of electronic data stored and accessed digitally from a computer system.

- Shortlink:-the short code is the small random-looking piece at the end of a short link.
ex: http://localhost:3000/abc123 -> abc123 is the short code


# FRONT-END

- Invalid URL or server failure: Show a small red message under the input box, like “Please enter a valid URL” or “Something went wrong, try again.” Keep the user’s text in the box so they can fix it.
- Delay after clicking: Change the button text to “Shortening...” and disable it until the result arrives. This prevents double clicks.
- Copy confirmation: Briefly change the button or icon to “Copied!” for about 2 seconds, then switch it back.
- Empty input: Don’t send anything. Show a message like “Please enter a URL” (or disable the button until something is typed).

# BACK-EDN
- So it sends the URL to somewhere that stays alive all the time. That somewhere is the backend (the server).

-The backend’s job, in plain words:

Receive the URL from the frontend
Check it (is it a real URL?)
Decide a short code
Save the pair somewhere permanent
Send the short link back

- What you nailed:

Check if it already exists. That’s the “same URL twice” decision we talked about. You chose to return the existing short link, which is a valid and common choice.
Check the URL format. Correct. This is called validation.
Key-value storage. A hashmap is exactly the right mental model. The short code is the key, the long URL is the value.