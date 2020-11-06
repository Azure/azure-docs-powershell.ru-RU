---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/update-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 6236a03b22bd3509933d58579db3e84d48723b68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568433"
---
# <span data-ttu-id="22084-101">Update-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="22084-101">Update-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="22084-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="22084-102">SYNOPSIS</span></span>
<span data-ttu-id="22084-103">Изменяет экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="22084-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22084-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="22084-104">SYNTAX</span></span>

### <span data-ttu-id="22084-105">ByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="22084-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22084-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="22084-106">ByResourceId</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22084-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="22084-107">ByInputObject</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22084-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22084-108">DESCRIPTION</span></span>
<span data-ttu-id="22084-109">Командлет Update-AzureRmPowerBIEmbeddedCapacity изменяет экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="22084-109">The Update-AzureRmPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="22084-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="22084-110">EXAMPLES</span></span>

### <span data-ttu-id="22084-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="22084-111">Example 1</span></span>
```
PS C:\> Update-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com, testuser2@contoso.com" -PassThru
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

<span data-ttu-id="22084-112">Изменяет пропускную способность с именем testcapacity в resourcegroup testgroup, чтобы установить теги в формате key1: value1 и key2: value2 и администратору. testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="22084-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="22084-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="22084-113">PARAMETERS</span></span>

### <span data-ttu-id="22084-114">-Администратор</span><span class="sxs-lookup"><span data-stu-id="22084-114">-Administrator</span></span>
<span data-ttu-id="22084-115">Имена пропускной способности, разделенные запятыми, которые нужно установить в качестве администратора емкости</span><span class="sxs-lookup"><span data-stu-id="22084-115">A comma separated capacity names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="22084-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22084-116">-DefaultProfile</span></span>
<span data-ttu-id="22084-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22084-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22084-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22084-118">-InputObject</span></span>
<span data-ttu-id="22084-119">Объект ввода для трубопроводов</span><span class="sxs-lookup"><span data-stu-id="22084-119">Input object for Piping</span></span>

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

### <span data-ttu-id="22084-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="22084-120">-Name</span></span>
<span data-ttu-id="22084-121">Имя встроенной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="22084-121">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="22084-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22084-122">-PassThru</span></span>
<span data-ttu-id="22084-123">При успешном завершении операции будут возвращены сведения об удаленной пропуске.</span><span class="sxs-lookup"><span data-stu-id="22084-123">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="22084-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22084-124">-ResourceGroupName</span></span>
<span data-ttu-id="22084-125">Имя группы ресурсов Azure, к которой относится емкость</span><span class="sxs-lookup"><span data-stu-id="22084-125">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="22084-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22084-126">-ResourceId</span></span>
<span data-ttu-id="22084-127">ИД ресурса встроенной мощности PowerBI.</span><span class="sxs-lookup"><span data-stu-id="22084-127">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="22084-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="22084-128">-Sku</span></span>
<span data-ttu-id="22084-129">Название SKU для производственной мощности.</span><span class="sxs-lookup"><span data-stu-id="22084-129">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="22084-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="22084-130">-Tag</span></span>
<span data-ttu-id="22084-131">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов в пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="22084-131">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="22084-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22084-132">-Confirm</span></span>
<span data-ttu-id="22084-133">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="22084-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="22084-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22084-134">-WhatIf</span></span>
<span data-ttu-id="22084-135">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="22084-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="22084-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22084-136">CommonParameters</span></span>
<span data-ttu-id="22084-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="22084-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22084-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22084-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22084-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="22084-139">INPUTS</span></span>

### <span data-ttu-id="22084-140">System. String</span><span class="sxs-lookup"><span data-stu-id="22084-140">System.String</span></span>

### <span data-ttu-id="22084-141">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="22084-141">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="22084-142">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="22084-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="22084-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="22084-143">OUTPUTS</span></span>

### <span data-ttu-id="22084-144">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="22084-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="22084-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="22084-145">NOTES</span></span>

## <span data-ttu-id="22084-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22084-146">RELATED LINKS</span></span>

[<span data-ttu-id="22084-147">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="22084-147">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="22084-148">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="22084-148">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
