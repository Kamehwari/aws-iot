const AWS     =   require('aws-sdk');
const iotData = new AWS.IotData({endpoint:AWSENDPOINT,secretAccessKey:SECRETKEY,accessKeyId : ACCESSKEY,region:'us-east-1', apiVersion:'2015-05-28'});
const iotParams = {
            payload: JSON.stringify({"message":"Hi"}),
            topic: 'topic1',
            qos:0};
module.exports.publish = (event, content)=>{
//iotData.publish is an asynchronous function and return statement //should be inside the callback .
    iotData.publish(iotParams, (err, data) =>{
      if(err)
          return {'statusCode': 500,'body':        JSON.stringify({'status':false})}
      else
          return {'statusCode': 200,'body':JSON.stringify({'status':true})
     }
}
