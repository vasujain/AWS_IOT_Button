# AWS_IOT_Button

## SNS_policy.json
 * NOTE: Lambda function's execution role needs specific permissions for SNS operations.
 * The policy JSON document available at SNS_policy.json . 
 * Select an execution role for this function, choose `Basic execution role`
 * In the new tab that open, expand `View Policy Document`, click Edit, and replace the entire policy document with the copied one at `https://github.com/vasujain/AWS_IOT_Button/blob/master/SNS_policy.json`
 * Then, click Allow to create your new execution role.
    
## button_payload.json
 * The following JSON template shows what is sent as the payload:
```json
    {
        "serialNumber": "GXXXXXXXXXXXXXXXXX",
        "batteryVoltage": "xxmV",
        "clickType": "SINGLE" | "DOUBLE" | "LONG"
    }
```
 * A "LONG" clickType is sent if the first press lasts longer than 1.5 seconds.
 * "SINGLE" and "DOUBLE" clickType payloads are sent for short clicks.
 * More documentation : http://docs.aws.amazon.com/iot/latest/developerguide/iot-lambda-rule.html
