# Usage
```
export FROM_EMAIL=sender@example.com
export TO_EMAIL=recipient@example.com
export PASSWD_SMTP=securepass
export USER_SMTP=username
export SMTP_EMAIL="host:port"
export SUBJECT_EMAIL="This should be the email subject"
export CONTENT_EMAIL="This is the content/body of email"
docker run -v $(pwd):/attachments --rm oaktondigital/sendemail-docker bash -c "sendEmail -u $SUBJECT_EMAIL -m $CONTENT_EMAIL -f $FROM_EMAIL -t $TO_EMAIL -s $SMTP_EMAIL -o tls=yes -xu $USER_SMTP -xp $PASSWD_SMTP"
```

# Attachments
add to command
```
-a <attachment>
```
