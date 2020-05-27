---
title: Обращение к ресурсам Azure и форматирование результатов | Документация Майкрософт
description: Как обратиться к ресурсам в Azure и форматировать результаты запроса.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 23cc0d13e9ecb17bef04cedc8a0f395a04e89390
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386482"
---
# <a name="querying-for-azure-resources"></a><span data-ttu-id="b17df-103">Обращение к ресурсам Azure</span><span class="sxs-lookup"><span data-stu-id="b17df-103">Querying for Azure resources</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="b17df-104">Вы можете обращаться к ресурсам с помощью встроенных командлетов PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b17df-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="b17df-105">В PowerShell имена командлетов представлены в формате **_глагол-существительное_**.</span><span class="sxs-lookup"><span data-stu-id="b17df-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="b17df-106">Командлеты, в которых используется глагол **_Get_** (Получить) — это командлеты запроса.</span><span class="sxs-lookup"><span data-stu-id="b17df-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="b17df-107">Существительные командлета — это типы ресурсов Azure, к которым будет применено действие командлета.</span><span class="sxs-lookup"><span data-stu-id="b17df-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>

## <a name="selecting-simple-properties"></a><span data-ttu-id="b17df-108">Выбор простых свойств</span><span class="sxs-lookup"><span data-stu-id="b17df-108">Selecting simple properties</span></span>

<span data-ttu-id="b17df-109">Для каждого командлета Azure PowerShell определено форматирование по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b17df-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="b17df-110">Самые распространенные свойства каждого типа ресурсов автоматически отображаются в формате таблицы или списка.</span><span class="sxs-lookup"><span data-stu-id="b17df-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="b17df-111">Дополнительные сведения о форматировании выходных данных см. в статье о [форматировании результатов запроса](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="b17df-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="b17df-112">Используйте командлет `Get-AzureRmVM`, чтобы получить список виртуальных машин своей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b17df-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```powershell-interactive
Get-AzureRmVM
```

<span data-ttu-id="b17df-113">Результаты по умолчанию автоматически форматируются в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="b17df-113">The default output is automatically formatted as a table.</span></span>

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="b17df-114">Командлет `Select-Object` можно использовать для выбора определенных свойств, которые вас интересуют.</span><span class="sxs-lookup"><span data-stu-id="b17df-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```powershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a><span data-ttu-id="b17df-115">Выбор сложных вложенных свойств</span><span class="sxs-lookup"><span data-stu-id="b17df-115">Selecting complex nested properties</span></span>

<span data-ttu-id="b17df-116">Если вы хотите выбрать свойства, которые глубоко вложены в выходные данные JSON, необходимо указать полный путь к такому свойству.</span><span class="sxs-lookup"><span data-stu-id="b17df-116">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="b17df-117">Следующий пример показывает, как выбрать имя виртуальной машины и тип ОС с помощью командлета `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="b17df-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```powershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a><span data-ttu-id="b17df-118">Фильтрация результатов с помощью командлета Where-Object</span><span class="sxs-lookup"><span data-stu-id="b17df-118">Filter result using the Where-Object cmdlet</span></span>

<span data-ttu-id="b17df-119">Командлет `Where-Object` позволяет фильтровать результаты на основе любого значения свойства.</span><span class="sxs-lookup"><span data-stu-id="b17df-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="b17df-120">В следующем примере фильтр выбирает только виртуальные машины, имя которых содержит текст RGD.</span><span class="sxs-lookup"><span data-stu-id="b17df-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```powershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="b17df-121">В следующем примере результаты вернут виртуальные машины размера Standard_DS1_V2.</span><span class="sxs-lookup"><span data-stu-id="b17df-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```powershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
