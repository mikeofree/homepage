![image](https://github.com/user-attachments/assets/34de0be4-5c21-4484-bb20-25671147d5f6)

I've been looking for a custom api widget I could use on my homepage to display my location and WAN IP. Doesn't have a huge use case but if anyone else was interested, here it is. json formatting applies and it only works on services.yaml. [Here's](https://ip-api.com/) a link to the api to see the custom fields you can also apply. 
[icons](https://github.com/walkxcode/dashboard-icons/blob/main/ICONS.md)

![image](https://github.com/user-attachments/assets/5f587b67-d88a-4972-8333-9ed3a87871b7)


```
    - Wan IP:
        icon: {insert-icon.png} #edit this if you want a icoon
        widget:
         type: customapi
         url: http://ip-api.com/json/
         refreshInterval: 10000 # optional - in milliseconds, defaults to 10s
         method: GET
         mappings:
         - field: 'city' 
           label: City 
           format: text
         - field: 'regionName'
           label: State
           format: text
         - field: 'query'
           label: WAN IP
           format: text
```
