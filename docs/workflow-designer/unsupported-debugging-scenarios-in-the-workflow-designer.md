---
title: "Unsupported debugging scenarios in the Workflow Designer | Microsoft Docs"
ms.date: "11/04/2016"
ms.topic: "reference"
ms.assetid: 6adbe379-41d0-4681-9cd0-b91f187c3c2c
ms.author: gewarren
manager: ghogen
ms.workload: 
  - "multiple"
author: gewarren
---
# Unsupported debugging scenarios in the Workflow Designer
The Workflow Designer in [!INCLUDE[netfx40_short](../workflow-designer/includes/netfx40_short_md.md)] added many new features, but there are still some debugging scenarios that it does not support. This document details unsupported Workflow Designer debugging scenarios.  
  
-   Execution cannot be continued after code has been edited.  
  
-   Execution cannot be continued from an arbitrary point in the workflow (Set Next).  
  
-   Execution cannot be continued until the cursor is reached (Run to Cursor).  
  
-   The workflow designer cannot be used to debug workflows created in code without the use of the designer.  
  
-   Workflows created in earlier versions of [!INCLUDE[wf](../workflow-designer/includes/wf_md.md)] cannot be debugged in the [!INCLUDE[netfx40_short](../workflow-designer/includes/netfx40_short_md.md)] designer.  
  
-   Breakpoints cannot be defined on links between activities or <xref:System.Activities.Statements.Flowchart> nodes.  
  
-   The clipboard is not available during debugging.  
  
-   Breakpoints are not retained when activities are copied or pasted.  
  
-   Workflow breakpoints cannot be set in the call stack window.  
  
-   When creating breakpoints in the designer, the **Line** and **Character** settings in the **New Breakpoint** dialog are not used.  
  
-   The Breakpoint window or shortcut menu does not support the following columns or options for workflow debugging:  
  
    -   Condition  
  
    -   Hit Count  
  
    -   When Hit  
  
    -   Function  
  
    -   Data  
  
    -   Process  
  
    -   Go to Disassembly