I am not sure how would I fetch the comma delimited list of URL’s using bash.
But given my limited understanding I would do the following;



I would use bash and use a cron job to be able to ping the website every 5 minutes and mail the output
*/5 /usr/bin/wget "www.example.com" --timeout 30 -O - 2>/dev/null  | grep "Normal operation string" || echo "The site is down" | /usr/bin/mail -v -s "Site is down" your@e-mail.address




