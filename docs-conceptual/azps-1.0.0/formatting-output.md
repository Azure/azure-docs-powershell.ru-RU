---
title: Форматирование выходных данных командлетов Azure PowerShell
description: Сведения о том, как форматировать выходные данные командлетов для Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/07/2019
ms.openlocfilehash: d655be02df40049d82d686667684b7b26a2c19ea
ms.sourcegitcommit: 460e10c867a07836c863177421ceb991aa083b40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/09/2019
ms.locfileid: "54136298"
---
# <a name="format-azurepowershell-cmdlet-output"></a><span data-ttu-id="99c32-103">Форматирование выходных данных командлетов Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="99c32-103">Format AzurePowerShell cmdlet output</span></span>

<span data-ttu-id="99c32-104">По умолчанию каждый командлет Azure PowerShell выводит выходные данные в удобном для чтения формате.</span><span class="sxs-lookup"><span data-stu-id="99c32-104">By default each Azure PowerShell cmdlet formats output to be easy to read.</span></span> <span data-ttu-id="99c32-105">PowerShell позволяет преобразовать или отформатировать выходные данные командлета, передав их в один из следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="99c32-105">PowerShell allows you to convert or format cmdlet output by piping to one of the following cmdlets:</span></span>

| <span data-ttu-id="99c32-106">Форматирование</span><span class="sxs-lookup"><span data-stu-id="99c32-106">Formatting</span></span>      | <span data-ttu-id="99c32-107">Преобразование</span><span class="sxs-lookup"><span data-stu-id="99c32-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="99c32-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="99c32-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="99c32-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="99c32-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="99c32-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="99c32-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="99c32-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="99c32-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="99c32-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="99c32-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="99c32-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="99c32-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="99c32-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="99c32-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="99c32-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="99c32-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

<span data-ttu-id="99c32-116">Форматирование используется для отображения данных в терминале PowerShell, а преобразование — для создания данных, используемых в других скриптах или программах.</span><span class="sxs-lookup"><span data-stu-id="99c32-116">Formatting is used for display in a PowerShell terminal, and conversion is used for generating data to be consumed by other scripts or programs.</span></span>

## <a name="table-output-format"></a><span data-ttu-id="99c32-117">Формат табличных выходных данных</span><span class="sxs-lookup"><span data-stu-id="99c32-117">Table output format</span></span>

<span data-ttu-id="99c32-118">По умолчанию выходные данные командлетов Azure PowerShell представлены в табличном формате.</span><span class="sxs-lookup"><span data-stu-id="99c32-118">By default, Azure PowerShell cmdlets output in the table format.</span></span> <span data-ttu-id="99c32-119">В таком формате отображаются не все сведения о запрашиваемом ресурсе.</span><span class="sxs-lookup"><span data-stu-id="99c32-119">This format doesn't display all information of the requested resource:</span></span>

```powershell-interactive
Get-AzVM
```

```output
ResourceGroupName           Name Location          VmSize  OsType               NIC ProvisioningState Zone
-----------------           ---- --------          ------  ------               --- ----------------- ----
QueryExample      ExampleLinuxVM  westus2        Basic_A0   Linux examplelinuxvm916         Succeeded
QueryExample         RHELExample  westus2  Standard_D2_v3   Linux    rhelexample469         Succeeded
QueryExample        WinExampleVM  westus2 Standard_DS1_v2 Windows   winexamplevm268         Succeeded
```

<span data-ttu-id="99c32-120">Объем данных, которые выводит командлет `Format-Table`, может зависеть от ширины окна сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="99c32-120">The amount of data displayed by `Format-Table` can be affected by the width of your PowerShell session window.</span></span> <span data-ttu-id="99c32-121">Чтобы ограничить выходные данные определенными свойствами и упорядочить эти данные, имена свойств можно указать в виде аргументов для `Format-Table`.</span><span class="sxs-lookup"><span data-stu-id="99c32-121">To restrict the output to specific properties and order them, property names can be provided as arguments to `Format-Table`:</span></span>

```powershell-interactive
Get-AzVM -ResourceGroupName QueryExample | Format-Table Name,ResourceGroupName,Location
```

```output
Name           ResourceGroupName Location
----           ----------------- --------
ExampleLinuxVM QueryExample      westus2
RHELExample    QueryExample      westus2
WinExampleVM   QueryExample      westus2
```

## <a name="list-output-format"></a><span data-ttu-id="99c32-122">Выходные данные в формате списка</span><span class="sxs-lookup"><span data-stu-id="99c32-122">List output format</span></span>

<span data-ttu-id="99c32-123">Выходные данные в формате списка представлены в двух столбцах: с именами свойств и значениями.</span><span class="sxs-lookup"><span data-stu-id="99c32-123">List output format produces two columns, property names followed by the value.</span></span> <span data-ttu-id="99c32-124">Для сложных объектов вместо этого отображается тип объекта.</span><span class="sxs-lookup"><span data-stu-id="99c32-124">For complex objects, the type of the object is displayed instead.</span></span>

```powershell-interactive
Get-AzVM | Format-List
```

<span data-ttu-id="99c32-125">В следующих выходных данных некоторые поля удалены.</span><span class="sxs-lookup"><span data-stu-id="99c32-125">The following output has some fields removed.</span></span>

```output
ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId                     : ...
Name                     : ExampleLinuxVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
...
StatusCode               : OK

ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/RHELExample
VmId                     : ...
Name                     : RHELExample
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
```

<span data-ttu-id="99c32-126">Как и при использовании `Format-Table`, вы можете упорядочить и ограничить выходные данные, указав имена свойств.</span><span class="sxs-lookup"><span data-stu-id="99c32-126">Like `Format-Table`, property names can be provided to order and restrict the output:</span></span>

```powershell-interactive
Get-AzVM | Format-List ResourceGroupName,Name,Location
```

```output
ResourceGroupName : QueryExample
Name              : ExampleLinuxVM
Location          : westus2

ResourceGroupName : QueryExample
Name              : RHELExample
Location          : westus2

ResourceGroupName : QueryExample
Name              : WinExampleVM
Location          : westus2
```

## <a name="wide-output-format"></a><span data-ttu-id="99c32-127">Выходные данные в широком формате</span><span class="sxs-lookup"><span data-stu-id="99c32-127">Wide output format</span></span>

<span data-ttu-id="99c32-128">При выводе данных в широком формате отображается только одно имя свойства на один запрос.</span><span class="sxs-lookup"><span data-stu-id="99c32-128">Wide output format produces only one property name per query.</span></span> <span data-ttu-id="99c32-129">Можно управлять тем, какие свойства должны отображаться, указав свойство в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="99c32-129">Which property is displayed can be controlled by giving a property as an argument.</span></span>

```powershell-interactive
Get-AzVM | Format-Wide
```

```output
ExampleLinuxVM                                  RHELExample
WinExampleVM
```

```powershell-interactive
Get-AzVM | Format-Wide ResourceGroupName
```

```output
QueryExample                                    QueryExample
QueryExample
```

## <a name="custom-output-format"></a><span data-ttu-id="99c32-130">Пользовательский формат выходных данных</span><span class="sxs-lookup"><span data-stu-id="99c32-130">Custom output format</span></span>

<span data-ttu-id="99c32-131">Тип выходных данных `Custom-Format` предназначен для форматирования пользовательских объектов.</span><span class="sxs-lookup"><span data-stu-id="99c32-131">The `Custom-Format` output type is meant for formatting custom objects.</span></span> <span data-ttu-id="99c32-132">Без аргументов он действует так же, как и `Format-List`, но выводит имена свойств пользовательских классов.</span><span class="sxs-lookup"><span data-stu-id="99c32-132">Without any arguments, it behaves like `Format-List` but displays the property names of custom classes.</span></span>

```powershell-interactive
Get-AzVM | Format-Custom
```

<span data-ttu-id="99c32-133">В следующих выходных данных некоторые поля удалены.</span><span class="sxs-lookup"><span data-stu-id="99c32-133">The following output has some fields removed.</span></span>

```output
ResourceGroupName : QueryExample
Id                : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId              : ...
Name              : ExampleLinuxVM
Type              : Microsoft.Compute/virtualMachines
Location          : westus2
Tags              : {}
HardwareProfile   : {VmSize}
NetworkProfile    : {NetworkInterfaces}
OSProfile         : {ComputerName, AdminUsername, LinuxConfiguration, Secrets,
AllowExtensionOperations}
ProvisioningState : Succeeded
StorageProfile    : {ImageReference, OsDisk, DataDisks}
...
```

<span data-ttu-id="99c32-134">Если задать имена свойств в качестве аргументов для `Custom-Format`, отобразятся пары "ключ — значение" для пользовательских объектов, заданных в качестве значений.</span><span class="sxs-lookup"><span data-stu-id="99c32-134">Giving property names as arguments to `Custom-Format` displays the property/value pairs for custom objects set as values:</span></span>

```powershell-interactive
Get-AzVM | Format-Custom Name,ResourceGroupName,Location,OSProfile
```

<span data-ttu-id="99c32-135">В следующих выходных данных некоторые поля удалены.</span><span class="sxs-lookup"><span data-stu-id="99c32-135">The following output has some fields removed.</span></span>

```output
class PSVirtualMachineList
{
  Name = ExampleLinuxVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = ExampleLinuxVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
      LinuxConfiguration =
        class LinuxConfiguration
        {
          DisablePasswordAuthentication = False
          Ssh =
          ProvisionVMAgent = True
        }
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}

...

class PSVirtualMachineList
{
  Name = WinExampleVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = WinExampleVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
        class WindowsConfiguration
        {
          ProvisionVMAgent = True
          EnableAutomaticUpdates = True
          TimeZone =
          AdditionalUnattendContent =
          WinRM =
        }
      LinuxConfiguration =
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}
```

## <a name="conversion-to-other-data-formats"></a><span data-ttu-id="99c32-136">Преобразование в другие форматы данных</span><span class="sxs-lookup"><span data-stu-id="99c32-136">Conversion to other data formats</span></span>

<span data-ttu-id="99c32-137">Семейство командлетов `ConvertTo-*` позволяет преобразовать результаты командлетов Azure PowerShell в машиночитаемый формат.</span><span class="sxs-lookup"><span data-stu-id="99c32-137">The `ConvertTo-*` family of cmdlets allows for converting the results of Azure PowerShell cmdlets to machine-readable formats.</span></span> <span data-ttu-id="99c32-138">Чтобы получить только некоторые свойства в результатах Azure PowerShell, используйте команду `Select-Object` при передаче до выполнения преобразования.</span><span class="sxs-lookup"><span data-stu-id="99c32-138">To get only some properties from the Azure PowerShell results, use the `Select-Object` command in a pipe before performing the conversion.</span></span> <span data-ttu-id="99c32-139">В следующих примерах показаны различные виды выходных данных после каждого преобразования.</span><span class="sxs-lookup"><span data-stu-id="99c32-139">The following examples demonstrate the different kinds of output that each conversion produces.</span></span>

### <a name="conversion-to-csv"></a><span data-ttu-id="99c32-140">Преобразование в CSV</span><span class="sxs-lookup"><span data-stu-id="99c32-140">Conversion to CSV</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-CSV
```

```output
#TYPE Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineList
"ResourceGroupName","Id","VmId","Name","Type","Location","LicenseType","Tags","AvailabilitySetReference","DiagnosticsProfile","Extensions","HardwareProfile","InstanceView","NetworkProfile","OSProfile","Plan","ProvisioningState","StorageProfile","DisplayHint","Identity","Zones","FullyQualifiedDomainName","AdditionalCapabilities","RequestId","StatusCode"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM","...","ExampleLinuxVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample","...","RHELExample","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM","...","WinExampleVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
```

### <a name="conversion-to-json"></a><span data-ttu-id="99c32-141">Преобразование в JSON</span><span class="sxs-lookup"><span data-stu-id="99c32-141">Conversion to JSON</span></span>

<span data-ttu-id="99c32-142">По умолчанию в выходных данных JSON развертываются не все свойства.</span><span class="sxs-lookup"><span data-stu-id="99c32-142">JSON output doesn't expand all properties by default.</span></span> <span data-ttu-id="99c32-143">Чтобы изменить глубину иерархии развернутых свойств, используйте аргумент `-Depth`.</span><span class="sxs-lookup"><span data-stu-id="99c32-143">To change the depth of properties expanded, use the `-Depth` argument.</span></span> <span data-ttu-id="99c32-144">По умолчанию для глубины иерархии указано `2`.</span><span class="sxs-lookup"><span data-stu-id="99c32-144">By default, the expansion depth is `2`.</span></span>

```azurepowershell-interactive
Get-AzVM|ConvertTo-JSON
```

<span data-ttu-id="99c32-145">В следующих выходных данных некоторые поля удалены.</span><span class="sxs-lookup"><span data-stu-id="99c32-145">The following output has some fields removed.</span></span>

```output
[
    {
        "ResourceGroupName":  "QUERYEXAMPLE",
        "Id":  "/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM",
        "VmId":  "...",
        "Name":  "ExampleLinuxVM",
        "Type":  "Microsoft.Compute/virtualMachines",
        "Location":  "westus2",
        ...
        "OSProfile":  {
                          "ComputerName":  "ExampleLinuxVM",
                          "AdminUsername":  "...",
                          "AdminPassword":  null,
                          "CustomData":  null,
                          "WindowsConfiguration":  null,
                          "LinuxConfiguration":  "Microsoft.Azure.Management.Compute.Models.LinuxConfiguration",
                          "Secrets":  "",
                          "AllowExtensionOperations":  true
                      },
        "Plan":  null,
        "ProvisioningState":  "Succeeded",
        "StorageProfile":  {
                               "ImageReference":  "Microsoft.Azure.Management.Compute.Models.ImageReference",
                               "OsDisk":  "Microsoft.Azure.Management.Compute.Models.OSDisk",
                               "DataDisks":  ""
                           },
        "DisplayHint":  0,
        "Identity":  null,
        "Zones":  [

                  ],
        "FullyQualifiedDomainName":  null,
        "AdditionalCapabilities":  null,
        "RequestId":  "...",
        "StatusCode":  200
    },
    ...
]
```

### <a name="conversion-to-xml"></a><span data-ttu-id="99c32-146">Преобразование в XML</span><span class="sxs-lookup"><span data-stu-id="99c32-146">Conversion to XML</span></span>

<span data-ttu-id="99c32-147">Командлет `ConvertTo-XML` позволяет преобразовать объект ответа Azure PowerShell в "чистый" объект XML, который может обрабатываться как любой другой объект XML в PowerShell.</span><span class="sxs-lookup"><span data-stu-id="99c32-147">The `ConvertTo-XML` cmdlet converts the Azure PowerShell response object into a pure XML object, which can be handled like any other XML object within PowerShell.</span></span> 

```azurepowershell-interactive
Get-AzVM | ConvertTo-XML
```

```output
xml                            Objects
---                            -------
version="1.0" encoding="utf-8" Objects
```

### <a name="conversion-to-html"></a><span data-ttu-id="99c32-148">Преобразование в HTML</span><span class="sxs-lookup"><span data-stu-id="99c32-148">Conversion to HTML</span></span>

<span data-ttu-id="99c32-149">При преобразовании объекта в HTML выходные данные будут отображаться в виде HTML-таблицы.</span><span class="sxs-lookup"><span data-stu-id="99c32-149">Converting an object to HTML produces output that will be rendered as an HTML table.</span></span> <span data-ttu-id="99c32-150">Преобразование HTML-кода для просмотра будет зависеть от настроек браузера для отображения таблиц, которые не содержат информацию о ширине.</span><span class="sxs-lookup"><span data-stu-id="99c32-150">Rendering of the HTML will depend on your browser behavior for rendering tables which contain no width information.</span></span>
<span data-ttu-id="99c32-151">Объекты пользовательского класса не развертываются.</span><span class="sxs-lookup"><span data-stu-id="99c32-151">No custom class objects are expanded.</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-HTML
```

```output
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>HTML TABLE</title>
</head><body>
<table>
<colgroup><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/></colgroup>
<tr><th>ResourceGroupName</th><th>Id</th><th>VmId</th><th>Name</th><th>Type</th><th>Location</th><th>LicenseType</th><th>Tags</th><th>AvailabilitySetReference</th><th>DiagnosticsProfile</th><th>Extensions</th><th>HardwareProfile</th><th>InstanceView</th><th>NetworkProfile</th><th>OSProfile</th><th>Plan</th><th>ProvisioningState</th><th>StorageProfile</th><th>DisplayHint</th><th>Identity</th><th>Zones</th><th>FullyQualifiedDomainName</th><th>AdditionalCapabilities</th><th>RequestId</th><th>StatusCode</th></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM</td><td>...</td><td>ExampleLinuxVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample</td><td>...</td><td>RHELExample</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM</td><td>...</td><td>WinExampleVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
</table>
</body></html>
```