---
title: Форматирование результатов запроса | Документация Майкрософт
description: Как обратиться к ресурсам в Azure и форматировать результаты запроса.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 9ae0d661630bf4e080b3bbaa7f357c384ef68cc4
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "52586825"
---
# <a name="formatting-query-results"></a><span data-ttu-id="5c1e6-103">Форматирование результатов запроса</span><span class="sxs-lookup"><span data-stu-id="5c1e6-103">Formatting query results</span></span>

<span data-ttu-id="5c1e6-104">По умолчанию каждый командлет PowerShell заранее определяет форматирование выходных данных, что упрощает их чтение.</span><span class="sxs-lookup"><span data-stu-id="5c1e6-104">By default each PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="5c1e6-105">Среда PowerShell также позволяет гибко настраивать выходные данные или преобразовать выходные данные командлета в другой формат с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="5c1e6-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="5c1e6-106">Форматирование</span><span class="sxs-lookup"><span data-stu-id="5c1e6-106">Formatting</span></span>      | <span data-ttu-id="5c1e6-107">Преобразование</span><span class="sxs-lookup"><span data-stu-id="5c1e6-107">Conversion</span></span>       |
|-----------------|------------------|
| `Format-Custom` | `ConvertTo-Csv`  |
| `Format-List`   | `ConvertTo-Html` |
| `Format-Table`  | `ConvertTo-Json` |
| `Format-Wide`   | `ConvertTo-Xml`  |

## <a name="formatting-examples"></a><span data-ttu-id="5c1e6-108">Примеры форматирования</span><span class="sxs-lookup"><span data-stu-id="5c1e6-108">Formatting examples</span></span>

<span data-ttu-id="5c1e6-109">В этом примере мы получаем список виртуальных машин Azure в нашей подписке по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5c1e6-109">In this example we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="5c1e6-110">Стандартные выходные данные команды Get-AzureRmVM в табличном формате.</span><span class="sxs-lookup"><span data-stu-id="5c1e6-110">The Get-AzureRmVM command defaults output into a table format.</span></span>

```powershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="5c1e6-111">Если вы хотите ограничить число возвращаемых столбцов, используйте командлет `Format-Table`.</span><span class="sxs-lookup"><span data-stu-id="5c1e6-111">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="5c1e6-112">В следующем примере мы получим тот же список виртуальных машин, но ограничим выходные данные: они будут отображать только имя виртуальной машины, группу ресурсов и расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5c1e6-112">In the following example we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="5c1e6-113">Параметр `-Autosize` изменяет размеры столбцов в соответствии с размером данных.</span><span class="sxs-lookup"><span data-stu-id="5c1e6-113">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```powershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="5c1e6-114">При необходимости вы можете просматривать сведения в формате списка.</span><span class="sxs-lookup"><span data-stu-id="5c1e6-114">If you would prefer you can view information in a list format.</span></span> <span data-ttu-id="5c1e6-115">В следующем примере показано, как использовать командлет `Format-List`.</span><span class="sxs-lookup"><span data-stu-id="5c1e6-115">The following example shows this using the`Format-List` cmdlet.</span></span>

```powershell-interactive
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

## <a name="converting-to-other-data-types"></a><span data-ttu-id="5c1e6-116">Преобразование в другие типы данных</span><span class="sxs-lookup"><span data-stu-id="5c1e6-116">Converting to other data types</span></span>

<span data-ttu-id="5c1e6-117">Среда PowerShell также предлагает несколько форматов выходных данных, которые можно использовать в зависимости от ваших потребностей.</span><span class="sxs-lookup"><span data-stu-id="5c1e6-117">PowerShell also offers multiple output format you can use to meet your needs.</span></span>  <span data-ttu-id="5c1e6-118">В следующем примере мы используем `Select-Object`, чтобы получить атрибуты виртуальных машин в нашей подписке и преобразовать выходные данные в формат CSV, который можно легко импортировать в базу данных или электронную таблицу.</span><span class="sxs-lookup"><span data-stu-id="5c1e6-118">In the following example we use the `Select-Object` cmdlet to get attributes of the virtual machines in our subscription and and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```powershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="5c1e6-119">Выходные данные также можно преобразовать в формат JSON.</span><span class="sxs-lookup"><span data-stu-id="5c1e6-119">You can also convert the output into JSON format.</span></span>  <span data-ttu-id="5c1e6-120">В следующем примере создается тот же список виртуальных машин, но формат выходных данных меняется на JSON.</span><span class="sxs-lookup"><span data-stu-id="5c1e6-120">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```powershell-interactive
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
