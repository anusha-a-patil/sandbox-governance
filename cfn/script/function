import json
import logging

logger = logging.getLogger()
logger.setLevel(logging.INFO)

def handler(event, context):
    try:
        for record in event['Records']:
            # Log the received message
            logger.info(f"Received message: {record['body']}")
            
            # Parse the message body
            message = json.loads(record['body'])
            
            # Process the message (add your business logic here)
            logger.info(f"Processing message: {message}")
            
        return {
            'statusCode': 200,
            'body': json.dumps({'message': 'Successfully processed messages'})
        }
        
    except Exception as e:
        logger.error(f"Error processing message: {str(e)}")
        raise e
