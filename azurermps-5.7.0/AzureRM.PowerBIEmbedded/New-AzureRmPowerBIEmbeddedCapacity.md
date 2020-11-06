---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 6badeec8b2425a5ca8e10dc88039a1d28e055cc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560188"
---
# <span data-ttu-id="931cb-101">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="931cb-101">New-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="931cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="931cb-102">SYNOPSIS</span></span>
<span data-ttu-id="931cb-103">Создает новую внедренную емкость PowerBI.</span><span class="sxs-lookup"><span data-stu-id="931cb-103">Creates a new PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="931cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="931cb-104">SYNTAX</span></span>

```
New-AzureRmPowerBIEmbeddedCapacity 
    [-ResourceGroupName] <String> 
    [-Name] <String> 
    [-Location] <String>
    [-Sku] <String> 
    [-Administrator] <String>
    [[-Tag] <Hashtable>] 
    [-WhatIf] 
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="931cb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="931cb-105">DESCRIPTION</span></span>
<span data-ttu-id="931cb-106">Командлет New-AzureRmPowerBIEmbeddedCapacity создает новую пропускную способность PowerBI Embedded.</span><span class="sxs-lookup"><span data-stu-id="931cb-106">The New-AzureRmPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="931cb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="931cb-107">EXAMPLES</span></span>

### <span data-ttu-id="931cb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="931cb-108">Example 1</span></span>
```
PS C:\> New-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="931cb-109">Создает емкость с именем testcapacity в области "Центральная часть США и в группе ресурсов" в Azure Region testRG.</span><span class="sxs-lookup"><span data-stu-id="931cb-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="931cb-110">Уровень SKU для производственной мощности будет равен a1.</span><span class="sxs-lookup"><span data-stu-id="931cb-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="931cb-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="931cb-111">PARAMETERS</span></span>

### <span data-ttu-id="931cb-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="931cb-112">-ResourceGroupName</span></span>
<span data-ttu-id="931cb-113">Имя группы ресурсов Azure, к которой относится емкость</span><span class="sxs-lookup"><span data-stu-id="931cb-113">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="931cb-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="931cb-114">-Name</span></span>
<span data-ttu-id="931cb-115">Имя встроенной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="931cb-115">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="931cb-116">-Location</span><span class="sxs-lookup"><span data-stu-id="931cb-116">-Location</span></span>
<span data-ttu-id="931cb-117">Регион Azure, на котором размещена емкость для PowerBI Embedded</span><span class="sxs-lookup"><span data-stu-id="931cb-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="931cb-118">-SKU</span><span class="sxs-lookup"><span data-stu-id="931cb-118">-Sku</span></span>
<span data-ttu-id="931cb-119">Название SKU для производственной мощности.</span><span class="sxs-lookup"><span data-stu-id="931cb-119">The name of the Sku for the capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="931cb-120">-Администратор</span><span class="sxs-lookup"><span data-stu-id="931cb-120">-Administrator</span></span>
<span data-ttu-id="931cb-121">Имена пропускной способности, разделенные запятыми, которые нужно установить в качестве администратора емкости</span><span class="sxs-lookup"><span data-stu-id="931cb-121">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="931cb-122">-Тег</span><span class="sxs-lookup"><span data-stu-id="931cb-122">-Tag</span></span>
<span data-ttu-id="931cb-123">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов в пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="931cb-123">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="931cb-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="931cb-124">-Confirm</span></span>
<span data-ttu-id="931cb-125">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="931cb-125">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="931cb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="931cb-126">-WhatIf</span></span>
<span data-ttu-id="931cb-127">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="931cb-127">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="931cb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="931cb-128">CommonParameters</span></span>
<span data-ttu-id="931cb-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="931cb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="931cb-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="931cb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="931cb-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="931cb-131">INPUTS</span></span>

### <span data-ttu-id="931cb-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="931cb-132">None</span></span>
<span data-ttu-id="931cb-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="931cb-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="931cb-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="931cb-134">OUTPUTS</span></span>

### <span data-ttu-id="931cb-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="931cb-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="931cb-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="931cb-136">NOTES</span></span>

## <span data-ttu-id="931cb-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="931cb-137">RELATED LINKS</span></span>

[<span data-ttu-id="931cb-138">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="931cb-138">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="931cb-139">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="931cb-139">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
