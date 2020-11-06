---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/update-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 64e96f423748e8991abcf26b178a8bd6b893cf0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557275"
---
# <span data-ttu-id="4236a-101">Update-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4236a-101">Update-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4236a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4236a-102">SYNOPSIS</span></span>
<span data-ttu-id="4236a-103">Изменяет экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="4236a-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4236a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4236a-104">SYNTAX</span></span>

```
Update-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [[-Sku] <String>]
    [[-Tag] <Hashtable>] 
    [[-Administrator] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="4236a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4236a-105">DESCRIPTION</span></span>
<span data-ttu-id="4236a-106">Командлет Update-AzureRmPowerBIEmbeddedCapacity изменяет экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="4236a-106">The Update-AzureRmPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="4236a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4236a-107">EXAMPLES</span></span>

### <span data-ttu-id="4236a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4236a-108">Example 1</span></span>
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

<span data-ttu-id="4236a-109">Изменяет пропускную способность с именем testcapacity в resourcegroup testgroup, чтобы установить теги в формате key1: value1 и key2: value2 и администратору. testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="4236a-109">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="4236a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4236a-110">PARAMETERS</span></span>

### <span data-ttu-id="4236a-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4236a-111">-Name</span></span>
<span data-ttu-id="4236a-112">Имя встроенной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="4236a-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="4236a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4236a-113">-ResourceGroupName</span></span>
<span data-ttu-id="4236a-114">Имя группы ресурсов Azure, к которой относится емкость</span><span class="sxs-lookup"><span data-stu-id="4236a-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="4236a-115">-SKU</span><span class="sxs-lookup"><span data-stu-id="4236a-115">-Sku</span></span>
<span data-ttu-id="4236a-116">Название SKU для производственной мощности.</span><span class="sxs-lookup"><span data-stu-id="4236a-116">The name of the Sku for the capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="4236a-117">-Тег</span><span class="sxs-lookup"><span data-stu-id="4236a-117">-Tag</span></span>
<span data-ttu-id="4236a-118">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов в пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="4236a-118">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```
### <span data-ttu-id="4236a-119">-Администратор</span><span class="sxs-lookup"><span data-stu-id="4236a-119">-Administrator</span></span>
<span data-ttu-id="4236a-120">Имена пропускной способности, разделенные запятыми, которые нужно установить в качестве администратора емкости</span><span class="sxs-lookup"><span data-stu-id="4236a-120">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="4236a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4236a-121">-ResourceId</span></span>
<span data-ttu-id="4236a-122">ИД ресурса встроенной мощности PowerBI.</span><span class="sxs-lookup"><span data-stu-id="4236a-122">PowerBI Embedded Capacity ResourceID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4236a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4236a-123">-InputObject</span></span>
<span data-ttu-id="4236a-124">Объект ввода для трубопроводов</span><span class="sxs-lookup"><span data-stu-id="4236a-124">Input object for Piping</span></span>

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4236a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4236a-125">-PassThru</span></span>
<span data-ttu-id="4236a-126">При успешном завершении операции будут возвращены сведения об удаленной пропуске.</span><span class="sxs-lookup"><span data-stu-id="4236a-126">Will return the deleted capacity details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4236a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4236a-127">-Confirm</span></span>
<span data-ttu-id="4236a-128">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="4236a-128">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4236a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4236a-129">-WhatIf</span></span>
<span data-ttu-id="4236a-130">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="4236a-130">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4236a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4236a-131">CommonParameters</span></span>
<span data-ttu-id="4236a-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4236a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4236a-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4236a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4236a-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4236a-134">INPUTS</span></span>

### <span data-ttu-id="4236a-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="4236a-135">None</span></span>
<span data-ttu-id="4236a-136">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="4236a-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4236a-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4236a-137">OUTPUTS</span></span>

### <span data-ttu-id="4236a-138">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4236a-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4236a-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="4236a-139">NOTES</span></span>

## <span data-ttu-id="4236a-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4236a-140">RELATED LINKS</span></span>

[<span data-ttu-id="4236a-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4236a-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="4236a-142">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4236a-142">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
