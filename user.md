# API - User

**File Name:** admin.js  
**File Path:**  /server/routes/admin.js  
Contains all possible route which an admin can access about an user such as register, update, view, delete user details etc.

* **Contents:**
* [All User Details](https://strapmobile.com/docs/react-native-taxi-app-web-dashboard/v4.0.0/api/user#allUserDetails)
* [Specific User Details](https://strapmobile.com/docs/react-native-taxi-app-web-dashboard/v4.0.0/api/user#specificUserDetails)
* [User Stats Details](https://strapmobile.com/docs/react-native-taxi-app-web-dashboard/v4.0.0/api/user#userStatsDetails)

#### All User Details

1. **API Path:**
   api/admin/user
2. **Method:**
   GET
3. **Description:**
   * This route fetch user details of both rider and driver, those which are registered with the taxi-app application.
   * Renders paginated data.
   * Functionality:
     `./controllers/admin-user.js`
   * Parameter validation:
     `./config/para-validation.js`
4. **Parameters:**

   * | **Name** | req |
     | :--- | :--- |
     | **Type** | Object |
     | **Contains** | Query: {  limit: Number,  pageNo: Number } |
   * **Name:  **res

     **Type:  **Object

     **Description:**  
     Response object returned to the api which contains collection of user details.

5. **Response:**

   * Returns object with four properties:
     **success **\(bool\), **message , data **and **meta .**
   * **Data**
     field is an array of user object containing all the details of the user.
   * **Meta**  
     field contains fields related to pagination such as totalNoOfPages, currPageNo, limit etc.

   * **Http Code**: 200

     **Name**: returnObj

     **Type**: Array of object

#### Specific User Details

1. **API Path:**
   api/admin/user/:userId
2. **Method:**
   GET
3. **Description:**
   * This route fetch details of a specific user, either a rider or a driver.
   * Requires **user ID **as input parameter.
   * Functionality:
     `./controllers/admin-user.js`
4. **Parameters:**

   * | **Name** | req |
     | :--- | :--- |
     | **Type** | Object |
     | **Contains** | params: {  Name: userId,  Type: string } |
   * **Name: **res

     **Type: **Object

     **Description:**  
     Response object returned to the api which contains requested user details.

5. **Response:**

   * Returns object with three properties:
     **success **\(bool\), **message **and **data **
   * **Data : **field is an object containing the details of requested user.

   * **Http Code **: 200

     **Name**: returnObj

     **Type**: Object

#### User Stats Details

1. **API Path:**
   api/admin/user/userStatsChart
2. **Method:**
   GET
3. **Description:**
   * This route fetch the number of user \(rider and driver\) registered with the Taxi App.
   * Functionality:
     `./controllers/admin-user.js`
4. **Parameters:**

   * **Name: **req

     **Type: **Object

   * **Name: **res

     **Type: **Object

     **Description: **Response object returned to the api which contains number of users.

5. **Response:**

   * Returns object with three properties:
     **success **\(bool\), **message **and **data**
   * **Data**  
     field is an object which contains the computed no of rider and driver data.

   * **Http Code**: 200

     **Name **: returnObj

     **Type**: Object


