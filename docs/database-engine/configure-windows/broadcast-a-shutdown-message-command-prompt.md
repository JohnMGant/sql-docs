---
title: "Broadcast a Shutdown Message (Command Prompt) | Microsoft Docs"
description: Find out how to use the net send command to broadcast a message in SQL Server. See how to determine which users are currently connected to SQL Server.
ms.custom: ""
ms.date: "03/14/2017"
ms.prod: sql
ms.prod_service: high-availability
ms.reviewer: ""
ms.technology: configuration
ms.topic: conceptual
helpviewer_keywords: 
  - "SQL Server, stopping"
  - "named instances [SQL Server], broadcasting shutdown messages"
  - "shutdown message broadcast"
  - "broadcasting shutdown message"
  - "command prompt [SQL Server], broadcasting shutdown messages"
  - "default instances [SQL Server], broadcasting shutdown messages"
  - "stopping SQL Server"
ms.assetid: 9f20ccd5-d952-431d-ba12-339911af9430
author: rwestMSFT
ms.author: randolphwest
---
# Broadcast a Shutdown Message (Command Prompt)
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  This topic describes how to broadcast a shutdown message in [!INCLUDE[ssnoversion](../../includes/ssnoversion-md.md)] by using the **net send** command. In the message, include the time the instance of [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] will be stopped so that users can finish their tasks.  
  
##  <a name="SSMSProcedure"></a>  
  
#### To broadcast a shutdown message  
  
1.  From a command prompt, enter:  
  
     **net send /users "message"**  
  
     The **/users** option specifies that the message be sent to all users connected to the server  
  
> [!NOTE]  
>  The **net send** command requires the messenger service to be running on both the sending and the receiving computers. The messenger service is disabled by default on Windows Server 2003. For information about **net send**, see the Windows documentation.  
  
 On your network, it may be more appropriate to contact users by e-mail or the telephone. To determine which users are currently connected to [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)], use the Activity Monitor. For information on the Activity Monitor, see [Activity Monitor](../../relational-databases/performance-monitor/activity-monitor.md) and [Open Activity Monitor &#40;SQL Server Management Studio&#41;](../../relational-databases/performance-monitor/open-activity-monitor-sql-server-management-studio.md).  
  
## See Also  
 [Start, Stop, Pause, Resume, Restart the Database Engine, SQL Server Agent, or SQL Server Browser Service](../../database-engine/configure-windows/start-stop-pause-resume-restart-sql-server-services.md)  
  
  
