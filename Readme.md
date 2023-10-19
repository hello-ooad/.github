# OOAD-BACKEND-PROJECT

`user`:

- `/user`

    - `/signin`：登录

        - 查询参数：

        - `userPassword`

        - `userName`

        - 返回：

        - {

              "code": 501,
        
              "msg": "用户名不存在",
        
              "data": **null**,
        
              "dataCount": **null**

            }

        - {

              "code": 502,
        
              "msg": "用户名或密码错误",
        
              "data": **null**,
        
              "dataCount": **null**

            }

        - {

              "code": 200,
          
              "msg": "success!",
          
              "data": **null**,
          
              "dataCount": **null**

            }

    - `/list`：显示全部用户信息（包括账户，密码）需要权限：admin
      
        - 返回：
        - `userId`
        - `userName`
        - `userPassword`
        
    - `/new`：新增用户
        - 查询参数：
        - `userPassword`
        - `userName`
        - 返回：T/F
        
    - `/islogin`: 检查是否登录
    
        - 查询参数：null
        - 返回：
        - {

              "code": 401,
            
              "msg": "token 无效：549530c3-dd5d-4a46-8292-1d0585359f1f",
            
              "data": **null**,
            
              "dataCount": **null**

            }

        - {

              "code": 200,
              
              "msg": "success！",
              
              "data": [
              
                "student",
              
                "admin",
              
                "manager"
              
              ],
              
              "dataCount": **null**
    
            }
        
    - `/username`：查询用户名是否存在
    
        - 查询参数：
        - `userName`
        - 返回：
        - {
    
            "code": 200,
    
            "msg": "success!",
    
            "data": **null**,
    
            "dataCount": **null**

          }
        - {
    
            "code": 501,
    
            "msg": "用户名不存在",
    
            "data": **null**,
    
            "dataCount": **null**
    
          }
        
    - `/logout`：登出
    
        - 查询参数：
    
        - 返回：
    
        - {
    
          "code": 200,
    
          "msg": "success!",
    
          "data": **null**,
    
          "dataCount": **null**
    
          }