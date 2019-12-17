# Introduktion
Den här sidan innehåller information som kan vara bra att veta för nya utvecklare som börjar arbeta med det interna projektet med arbetsnamnet Bookit. Målet med projektet är att utveckla en webapplikation för att administrera evengemang (t.ex. fester och konferenser), typ som EventBrite men mer anpassat för just Knowit. 

# Kommunikationskanaler
Vi kommunicerar främst via vår Slack-kanal (knowit-event-app på knowit.slack.com (du måste skapa konto)) och ibland via Outlook. 

# Inloggning till verktyg vi använder
Vi har skapat en gemensam email för vårt team som kallas _eventapp@knowit.se_. Den använder vi vid registrering för olika verktyg för att inte medlemmarna i teamet ska vara hårt knutna till verktygen. För lösenord maila till _eventapp@knowit.se_ eller kontaka Erik S Johansson för kontaktuppgifter till teammedlemmarna. 

## Github
Vi har en gemensam inloggning via _eventapp@knowit.se_ och ett lösenord som distribueras via vår Slack-kanal. Vi använder det gemensamma kontot för att skapa och sätta upp repositories i Github, och sedan bjuder vi in våra privata konton till alla repositories. 

## Dockerhub
Vi har en gemensam inloggning via _eventapp@knowit.se_ och ett lösenord som distribueras via vår Slack-kanal.

## Amazon Web Services (AWS)
Vi har en gemensam inloggning via _eventapp@knowit.se_ och ett lösenord som distribueras via vår Slack-kanal. Det gemensamma kontot är skapat via AWS Organisations från Eriks konto för att ha gemensam betalning via hans konto. Vårt gemensamma konto har i sin tur skapat en AWS IAM user för varje person i teamet och det är via de kontona vi ska använda AWS. Skapa ett IAM User för dig och sedan tryck "Glömt Lösenord" när du loggar in första gången så får du skapa ett lösenord. 

## CircleCI
Logga in på vårt gemensamma konto på Github (dvs _eventapp@knowit.se_) och tryck på "logga in via Github" när du ska logga in på CircleCI.

# Versionshantering (GIT)

Teamets kod finns här:
https://github.com/ProTeamK60/

Klona följande repon:
- _bookit-ng_
- _bookit-event_
- _bookit-registration_
- _bookit-notification_
- _bookit-aws-lambda_

Vi brukar skapa feature-brancher när vi utvecklar en ny feature, som branchar ut från development. När vi känner att en featuren är klarr så mergar vi in den i branchen development via en pull request som ska kodgranskas av minst en annan i teamet. 

# Preparations

## Backend

###Bookit-event

Ladda ner OpenJDK 13 och peka ut den i din java classpath:
https://adoptopenjdk.net/

Du ska nu kunna bygga och köra bookit-event applikationen.
Kolla att får en json utskrift på följande GET anrop:

http://localhost:8080/api/v1/events

# Deployment
Vi använder Amazon Web Services (AWS) för deployment av vår applikation. 

# CI/CD
Vi använder oss för det mesta av CircleCIs pipelines, men även lite av AWS egna CodePipeline, CodeBuild och CodeDeploy.

# Teknologistack
- Java 13
- Spring Boot 2
- Angular 8
- Docker
