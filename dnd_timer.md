# Do Not Disturb settings

Note. This describes the information you see in the DND configuration page in the MiHome App.
The actual DND status comes from the status message

## Get details
### Command
| Key  | Value  | Comment  |
| ------- | ----------- | ------- |
| method | `get_dnd_timer` |  | 
| id   | [Integer] | is returned in the response used to link the send message to the response. |

#### Example
`{'method': 'get_dnd_timer', 'id': 2}`

### Response

|  Key  | Example | Description |
| ------------ |------ |------------------------------ |
| `enabled` |  _1_ | Is DND functionality Enabled (1=True) |
| `end_hour` |  _8_ |  End Time DND (hour part) |
| `end_minute` | _0_ |  End Time DND (minute part) |
|  `start_hour` | _22_ | Start Time DND (hour part) |
| `start_minute` | _0_ | Start Time DND (minute part |

#### Example Response

```
{
    "id": 2,
    "result": [
        {
            "enabled": 1,
            "end_hour": 8,
            "end_minute": 0,
            "start_hour": 22,
            "start_minute": 0
        }
    ]
}
```

## Set DND time

### Command
 Key  | Value  | Comment  |
| ------- | ----------- | ------- |
| method | `set_dnd_timer` |  | 
| params | `[start hour, start minutes, end hour, end minutes` | 24 hour notation, not using am/pm | 
| id   | [Integer] | is returned in the response used to link the send message to the response. |
#
### Example
`{'method': 'set_dnd_timer', 'params': [22,0,8,0] , 'id': 2}`


