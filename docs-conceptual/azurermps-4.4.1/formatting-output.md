---
title: Форматирование результатов запроса | Документация Майкрософт
description: Как обратиться к ресурсам в Azure и форматировать результаты запроса.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: a76ceee5ae1172630d74afd3c671031592d78a8b
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386771"
---
# <a name="formatting-query-results"></a><span data-ttu-id="b3c75-103">Форматирование результатов запроса</span><span class="sxs-lookup"><span data-stu-id="b3c75-103">Formatting query results</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="b3c75-104">По умолчанию каждый командлет PowerShell заранее определяет форматирование выходных данных, что упрощает их чтение.</span><span class="sxs-lookup"><span data-stu-id="b3c75-104">By default each PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="b3c75-105">Среда PowerShell также позволяет гибко настраивать выходные данные или преобразовать выходные данные командлета в другой формат с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="b3c75-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="b3c75-106">Форматирование</span><span class="sxs-lookup"><span data-stu-id="b3c75-106">Formatting</span></span>      | <span data-ttu-id="b3c75-107">Преобразование</span><span class="sxs-lookup"><span data-stu-id="b3c75-107">Conversion</span></span>       |
|-----------------|------------------|
| `Format-Custom` | `ConvertTo-Csv`  |
| `Format-List`   | `ConvertTo-Html` |
| `Format-Table`  | `ConvertTo-Json` |
| `Format-Wide`   | `ConvertTo-Xml`  |

## <a name="formatting-examples"></a><span data-ttu-id="b3c75-108">Примеры форматирования</span><span class="sxs-lookup"><span data-stu-id="b3c75-108">Formatting examples</span></span>

<span data-ttu-id="b3c75-109">В этом примере мы получаем список виртуальных машин Azure в нашей подписке по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b3c75-109">In this example we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="b3c75-110">Стандартные выходные данные команды Get-AzureRmVM в табличном формате.</span><span class="sxs-lookup"><span data-stu-id="b3c75-110">The Get-AzureRmVM command defaults output into a table format.</span></span>

```powershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="b3c75-111">Если вы хотите ограничить число возвращаемых столбцов, используйте командлет `Format-Table`.</span><span class="sxs-lookup"><span data-stu-id="b3c75-111">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="b3c75-112">В следующем примере мы получим тот же список виртуальных машин, но ограничим выходные данные: они будут отображать только имя виртуальной машины, группу ресурсов и расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b3c75-112">In the following example we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="b3c75-113">Параметр `-Autosize` изменяет размеры столбцов в соответствии с размером данных.</span><span class="sxs-lookup"><span data-stu-id="b3c75-113">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```powershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="b3c75-114">При необходимости вы можете просматривать сведения в формате списка.</span><span class="sxs-lookup"><span data-stu-id="b3c75-114">If you would prefer you can view information in a list format.</span></span> <span data-ttu-id="b3c75-115">В следующем примере показано, как использовать командлет `Format-List`.</span><span class="sxs-lookup"><span data-stu-id="b3c75-115">The following example shows this using the`Format-List` cmdlet.</span></span>

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

## <a name="converting-to-other-data-types"></a><span data-ttu-id="b3c75-116">Преобразование в другие типы данных</span><span class="sxs-lookup"><span data-stu-id="b3c75-116">Converting to other data types</span></span>

<span data-ttu-id="b3c75-117">Среда PowerShell также предлагает несколько форматов выходных данных, которые можно использовать в зависимости от ваших потребностей.</span><span class="sxs-lookup"><span data-stu-id="b3c75-117">PowerShell also offers multiple output format you can use to meet your needs.</span></span>  <span data-ttu-id="b3c75-118">В следующем примере мы используем `Select-Object`, чтобы получить атрибуты виртуальных машин в нашей подписке и преобразовать выходные данные в формат CSV, который можно легко импортировать в базу данных или электронную таблицу.</span><span class="sxs-lookup"><span data-stu-id="b3c75-118">In the following example we use the `Select-Object` cmdlet to get attributes of the virtual machines in our subscription and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```powershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="b3c75-119">Выходные данные также можно преобразовать в формат JSON.</span><span class="sxs-lookup"><span data-stu-id="b3c75-119">You can also convert the output into JSON format.</span></span>  <span data-ttu-id="b3c75-120">В следующем примере создается тот же список виртуальных машин, но формат выходных данных меняется на JSON.</span><span class="sxs-lookup"><span data-stu-id="b3c75-120">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

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
