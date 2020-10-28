# 2019-nCoV-Analysis

### How to run for the first time:

Navigate into project root using your command line client of choice.
Run the command:
```pip install -r requirements.txt``` 
to prepare environment.
Then, run the command 
```python application.py```
This will start the server at ```localhost:80```.  
The server will automatically pull updated data from the NYT and CDC sources (although the CDC has stopped updating their feed), update the database, and render the dashboard.

To deploy as an application using a service like AWS Elastic Beanstalk, edit the line in ```application.py```:
```app.run_server(debug=False, port=80)```
to say:
```application.run_server(debug=False, port=80)```.

This will pass the server object to the AWS backend, instead of the app object used to render the Dash app locally.
