# sample_ebapp
sample python app for ci-cd using elastic bean stack

#jenkins elastic bean stalk deploy automation

echo #step:1 initialise eb application
eb init my-eb --platform python-3.6 --region us-east-1
echo #step:2select development environment for deployment
eb use MyEb-env-1
echo #step:3 deploy the application
eb deploy
echo #step:4 get deployment health check and Status
eb health
eb status

Note: environment myeb-env-1 should exist prior to running above commands in jenkins post build action otherwise build fails
