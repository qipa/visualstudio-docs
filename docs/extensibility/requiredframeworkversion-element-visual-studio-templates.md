---
title: "RequiredFrameworkVersion Element (Visual Studio Templates) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology:
  - "vs-ide-general"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords:
  - "<RequiredFrameworkVersion> (Visual Studio Templates)"
  - "RequiredFrameworkVersion (Visual Studio Templates)"
ms.assetid: 08a4f609-51a5-4723-b89f-99277fb18871
caps.latest.revision: 10
author: "gregvanl"
ms.author: "gregvanl"
manager: ghogen
ms.workload:
  - "vssdk"
---
# RequiredFrameworkVersion Element (Visual Studio Templates)

Specifies the minimum version of the .NET Framework that is required by the template. It causes the **Target Framework Version** dropdown to be displayed in the **New Project** dialog. The `RequiredFrameworkVersion` element also determines the lowest value available in the dropdown.

> [!IMPORTANT]
> Starting in Visual Studio 2017 version 15.6, the **Target Framework Version** dropdown is no longer a filter for displayed templates in the **Templates** section of the **New Project** dialog. Instead, the dropdown functions as a framework picker for the selected template.

 \<VSTemplate>
 \<TemplateData>
 \<RequiredFrameworkVersion>

## Syntax

```xml
<RequiredFrameworkVersion> .... </RequiredFrameworkVersion>
```

## Attributes and Elements
 The following sections describe attributes, child elements, and parent elements.

### Attributes
 None.

### Child Elements
 None.

### Parent Elements

|Element|Description|
|-------------|-----------------|
|[TemplateData](../extensibility/templatedata-element-visual-studio-templates.md)|Required element.<br /><br /> Categorizes the template and defines how it is displayed in either the **New Project** or the **Add New Item** dialog box.|

## Text Value
 A text value is required.

 The text must be the minimum version number of the .NET Framework that is required for the template.

## Remarks

`RequiredFrameworkVersion` is an optional element. Use this element only if the template supports a specific minimum version (and later versions if any) of the .NET Framework. If you specify the `RequiredFrameworkVersion` element and your template doesn't support a specific minimum version of the .NET Framework, the **Target Framework Version** dropdown displays when it is not applicable.

## Example

The following example illustrates the metadata for a standard [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] class template.

```xml
<VSTemplate Type="Item" Version="3.0.0"
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">
    <TemplateData>
        <Name>MyClass</Name>
        <Description>My custom C# class template.</Description>
        <Icon>Icon.ico</Icon>
        <ProjectType>CSharp</ProjectType>
        <RequiredFrameworkVersion>3.0</RequiredFrameworkVersion>
        <MaxFrameworkVersion>4.7.1</MaxFrameworkVersion>
        <DefaultName>MyClass</DefaultName>
    </TemplateData>
    <TemplateContent>
        <ProjectItem>MyClass.cs</ProjectItem>
    </TemplateContent>
</VSTemplate>
```

In this example, the minimum version of the .NET Framework that is required by the template, represented by `RequiredFrameworkVersion`, is 3.0. A project created with this template can target .NET Framework versions starting from 3.0.

## See Also

- [Visual Studio Template Schema Reference](../extensibility/visual-studio-template-schema-reference.md)
- [Creating Project and Item Templates](../ide/creating-project-and-item-templates.md)
- [Targeting a Specific .NET Framework Version](../ide/targeting-a-specific-dotnet-framework-version.md)
