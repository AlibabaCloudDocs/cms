# Manage the service-linked role for Cloud Monitor

The service-linked role for Cloud Monitor, AliyunServiceRoleForCloudMonitor, is the Resource Access Management \(RAM\) role that authorizes Cloud Monitor to access other Alibaba Cloud services in specific scenarios.

**Note:** For more information about the service-linked role, see [Service-linked roles](/intl.en-US/RAM Role Management/Service-linked roles.md).

## Scenarios

When Cloud Monitor automatically installs the Cloud Monitor agent on hosts, Cloud Monitor uses the service-linked role to obtain the permission to use Cloud Assistant.

## Permission description

The following section describes the permissions of the service-linked role:

-   Name: AliyunServiceRoleForCloudMonitor
-   Policy attached to the role: AliyunServiceRolePolicyForCloudMonitor
-   Policy description: grants Cloud Monitor the permissions to use Cloud Assistant to view status, run commands, and view command output on all instances of the current account.

    ```
    {
        "Version": "1",
        "Statement": [
            {
                "Effect": "Allow",
                "Action": [
                    "ecs:RunCommand",
                    "ecs:DescribeInvocations",
                    "ecs:DescribeCloudAssistantStatus"
                ],
                "Resource": [
                    "acs:ecs:*:*:instance/*",
                    "acs:ecs:*:*:command/*"
                ]
            }
        ]
    }               
    ```


## Create the service-linked role

When Cloud Monitor automatically installs the Cloud Monitor agent on hosts, Cloud Monitor automatically creates the service-linked role.

## Delete the service-linked role

To delete the service-linked role, perform the following steps:

1.  On the Host Monitoring page, check whether **New purchase ECS automatically installs Cloud Monitor** is turned off.

    If **New purchase ECS automatically installs Cloud Monitor** is turned on, click the ![Switch](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/9850628951/p118024.png) icon to turn the switch off.

2.  Delete the service-linked role.

    For more information about how to delete the service-linked role, see [Delete the service-linked role AliyunServiceRoleForDAS](/intl.en-US/RAM Role Management/Service-linked roles.md).


