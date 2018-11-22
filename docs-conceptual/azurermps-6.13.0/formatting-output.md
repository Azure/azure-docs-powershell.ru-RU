---
title: Форматирование выходных данных командлетов Azure PowerShell
description: Сведения о том, как форматировать выходные данные командлетов для Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 390285bcf483e75b7a2b77d345ccb108669f66e5
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/22/2018
ms.locfileid: "52260015"
---
# <a name="format-azurepowershell-cmdlet-output"></a><span data-ttu-id="17f55-103">Форматирование выходных данных командлетов Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="17f55-103">Format AzurePowerShell cmdlet output</span></span>

<span data-ttu-id="17f55-104">По умолчанию каждый командлет Azure PowerShell заранее определяет форматирование выходных данных, что упрощает их чтение.</span><span class="sxs-lookup"><span data-stu-id="17f55-104">By default each Azure PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="17f55-105">Среда PowerShell также позволяет гибко настраивать выходные данные или преобразовать выходные данные командлета в другой формат с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="17f55-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="17f55-106">Форматирование</span><span class="sxs-lookup"><span data-stu-id="17f55-106">Formatting</span></span>      | <span data-ttu-id="17f55-107">Преобразование</span><span class="sxs-lookup"><span data-stu-id="17f55-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="17f55-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="17f55-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="17f55-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="17f55-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="17f55-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="17f55-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="17f55-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="17f55-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="17f55-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="17f55-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="17f55-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="17f55-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="17f55-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="17f55-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="17f55-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="17f55-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

## <a name="format-examples"></a><span data-ttu-id="17f55-116">Примеры форматирования</span><span class="sxs-lookup"><span data-stu-id="17f55-116">Format examples</span></span>

<span data-ttu-id="17f55-117">В этом примере показано, как получить список виртуальных машин Azure в подписке по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="17f55-117">In this example, we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="17f55-118">По умолчанию выходные данные команды `Get-AzureRmVM` представлены в табличном формате.</span><span class="sxs-lookup"><span data-stu-id="17f55-118">The `Get-AzureRmVM` command defaults output into a table format.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="17f55-119">Если вы хотите ограничить число возвращаемых столбцов, используйте командлет `Format-Table`.</span><span class="sxs-lookup"><span data-stu-id="17f55-119">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="17f55-120">В следующем примере показано, как получить тот же список виртуальных машин, но ограничить выходные данные так, чтобы они содержали только имя виртуальной машины, группу ресурсов и расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="17f55-120">In the following example, we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="17f55-121">Параметр `-Autosize` изменяет размеры столбцов в соответствии с размером данных.</span><span class="sxs-lookup"><span data-stu-id="17f55-121">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="17f55-122">Выходные данные также можно отформатировать в виде списка.</span><span class="sxs-lookup"><span data-stu-id="17f55-122">Output can also be formatted into a list.</span></span> <span data-ttu-id="17f55-123">В следующем примере показано, как использовать командлет `Format-List`.</span><span class="sxs-lookup"><span data-stu-id="17f55-123">The following example shows this using the`Format-List` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Format-List Name,VmId,Location,ResourceGroupName
```

```output
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="convert-to-other-data-types"></a><span data-ttu-id="17f55-124">Преобразование в другие типы данных</span><span class="sxs-lookup"><span data-stu-id="17f55-124">Convert to other data types</span></span>

<span data-ttu-id="17f55-125">При помощи PowerShell также можно получить выходные данные команды и преобразовать их в несколько форматов данных.</span><span class="sxs-lookup"><span data-stu-id="17f55-125">PowerShell also allows taking command output and converting it into multiple data formats.</span></span> <span data-ttu-id="17f55-126">В следующем примере описано, как использовать командлет `Select-Object`, чтобы получить атрибуты виртуальных машин в нашей подписке и преобразовать выходные данные в формат CSV, который можно легко импортировать в базу данных или электронную таблицу.</span><span class="sxs-lookup"><span data-stu-id="17f55-126">In the following example, the `Select-Object` cmdlet is used to get attributes of the virtual machines in our subscription and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="17f55-127">Выходные данные можно также преобразовать в формат JSON.</span><span class="sxs-lookup"><span data-stu-id="17f55-127">Output can also be converted into the JSON format.</span></span>  <span data-ttu-id="17f55-128">В следующем примере создается тот же список виртуальных машин, но формат выходных данных меняется на JSON.</span><span class="sxs-lookup"><span data-stu-id="17f55-128">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```output
[
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610",
        "VmId":  "33422f9b-e339-4704-bad8-dbe094585496",
        "Name":  "MyUnbuntu1610",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    },
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM",
        "VmId":  "4650c755-fc2b-4fc7-a5bc-298d5c00808f",
        "Name":  "MyWin2016VM",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    }
]
```
