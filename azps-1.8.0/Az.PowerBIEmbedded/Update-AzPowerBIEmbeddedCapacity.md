---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/update-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: bed116bedbd06919728da8727cad609813bfc2a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729788"
---
# <span data-ttu-id="e885c-101">Update-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e885c-101">Update-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e885c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e885c-102">SYNOPSIS</span></span>
<span data-ttu-id="e885c-103">Изменяет экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="e885c-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="e885c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e885c-104">SYNTAX</span></span>

### <span data-ttu-id="e885c-105">ByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e885c-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e885c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e885c-106">ByResourceId</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e885c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e885c-107">ByInputObject</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e885c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e885c-108">DESCRIPTION</span></span>
<span data-ttu-id="e885c-109">Командлет Update-AzPowerBIEmbeddedCapacity изменяет экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="e885c-109">The Update-AzPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="e885c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e885c-110">EXAMPLES</span></span>

### <span data-ttu-id="e885c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e885c-111">Example 1</span></span>
```
PS C:\> Update-AzPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com, testuser2@contoso.com" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}
```

<span data-ttu-id="e885c-112">Изменяет пропускную способность с именем testcapacity в resourcegroup testgroup, чтобы установить теги в формате key1: value1 и key2: value2 и администратору. testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="e885c-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="e885c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e885c-113">PARAMETERS</span></span>

### <span data-ttu-id="e885c-114">-Администратор</span><span class="sxs-lookup"><span data-stu-id="e885c-114">-Administrator</span></span>
<span data-ttu-id="e885c-115">Имена пропускной способности, разделенные запятыми, которые нужно установить в качестве администратора емкости</span><span class="sxs-lookup"><span data-stu-id="e885c-115">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e885c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e885c-116">-DefaultProfile</span></span>
<span data-ttu-id="e885c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e885c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e885c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e885c-118">-InputObject</span></span>
<span data-ttu-id="e885c-119">Объект ввода для трубопроводов</span><span class="sxs-lookup"><span data-stu-id="e885c-119">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e885c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e885c-120">-Name</span></span>
<span data-ttu-id="e885c-121">Имя встроенной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="e885c-121">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e885c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e885c-122">-PassThru</span></span>
<span data-ttu-id="e885c-123">При успешном завершении операции будут возвращены сведения об удаленной пропуске.</span><span class="sxs-lookup"><span data-stu-id="e885c-123">Will return the deleted capacity details if the operation completes successfully</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e885c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e885c-124">-ResourceGroupName</span></span>
<span data-ttu-id="e885c-125">Имя группы ресурсов Azure, к которой относится емкость</span><span class="sxs-lookup"><span data-stu-id="e885c-125">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e885c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e885c-126">-ResourceId</span></span>
<span data-ttu-id="e885c-127">ИД ресурса встроенной мощности PowerBI.</span><span class="sxs-lookup"><span data-stu-id="e885c-127">PowerBI Embedded Capacity ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e885c-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="e885c-128">-Sku</span></span>
<span data-ttu-id="e885c-129">Название SKU для производственной мощности.</span><span class="sxs-lookup"><span data-stu-id="e885c-129">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e885c-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="e885c-130">-Tag</span></span>
<span data-ttu-id="e885c-131">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов в пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="e885c-131">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e885c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e885c-132">-Confirm</span></span>
<span data-ttu-id="e885c-133">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="e885c-133">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e885c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e885c-134">-WhatIf</span></span>
<span data-ttu-id="e885c-135">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="e885c-135">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e885c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e885c-136">CommonParameters</span></span>
<span data-ttu-id="e885c-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e885c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e885c-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e885c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e885c-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e885c-139">INPUTS</span></span>

### <span data-ttu-id="e885c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e885c-140">System.String</span></span>

### <span data-ttu-id="e885c-141">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e885c-141">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e885c-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e885c-142">OUTPUTS</span></span>

### <span data-ttu-id="e885c-143">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e885c-143">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e885c-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="e885c-144">NOTES</span></span>

## <span data-ttu-id="e885c-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e885c-145">RELATED LINKS</span></span>

[<span data-ttu-id="e885c-146">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e885c-146">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="e885c-147">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e885c-147">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
