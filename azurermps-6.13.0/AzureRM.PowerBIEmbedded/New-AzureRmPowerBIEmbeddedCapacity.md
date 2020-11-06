---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8546dbfbe8da12cd61c8b03d8aca64772d032b60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564147"
---
# <span data-ttu-id="ae8d2-101">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="ae8d2-101">New-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="ae8d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae8d2-102">SYNOPSIS</span></span>
<span data-ttu-id="ae8d2-103">Создает новую внедренную емкость PowerBI.</span><span class="sxs-lookup"><span data-stu-id="ae8d2-103">Creates a new PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae8d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae8d2-104">SYNTAX</span></span>

```
New-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae8d2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae8d2-105">DESCRIPTION</span></span>
<span data-ttu-id="ae8d2-106">Командлет New-AzureRmPowerBIEmbeddedCapacity создает новую пропускную способность PowerBI Embedded.</span><span class="sxs-lookup"><span data-stu-id="ae8d2-106">The New-AzureRmPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="ae8d2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae8d2-107">EXAMPLES</span></span>

### <span data-ttu-id="ae8d2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ae8d2-108">Example 1</span></span>
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

<span data-ttu-id="ae8d2-109">Создает емкость с именем testcapacity в области "Центральная часть США и в группе ресурсов" в Azure Region testRG.</span><span class="sxs-lookup"><span data-stu-id="ae8d2-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="ae8d2-110">Уровень SKU для производственной мощности будет равен a1.</span><span class="sxs-lookup"><span data-stu-id="ae8d2-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="ae8d2-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae8d2-111">PARAMETERS</span></span>

### <span data-ttu-id="ae8d2-112">-Администратор</span><span class="sxs-lookup"><span data-stu-id="ae8d2-112">-Administrator</span></span>
<span data-ttu-id="ae8d2-113">Имена пропускной способности, разделенные запятыми, которые нужно установить в качестве администратора емкости</span><span class="sxs-lookup"><span data-stu-id="ae8d2-113">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae8d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae8d2-114">-DefaultProfile</span></span>
<span data-ttu-id="ae8d2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae8d2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae8d2-116">-Location</span><span class="sxs-lookup"><span data-stu-id="ae8d2-116">-Location</span></span>
<span data-ttu-id="ae8d2-117">Регион Azure, на котором размещена емкость для PowerBI Embedded</span><span class="sxs-lookup"><span data-stu-id="ae8d2-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae8d2-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ae8d2-118">-Name</span></span>
<span data-ttu-id="ae8d2-119">Имя встроенной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="ae8d2-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae8d2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae8d2-120">-ResourceGroupName</span></span>
<span data-ttu-id="ae8d2-121">Имя группы ресурсов Azure, к которой относится емкость</span><span class="sxs-lookup"><span data-stu-id="ae8d2-121">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae8d2-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="ae8d2-122">-Sku</span></span>
<span data-ttu-id="ae8d2-123">Название SKU для производственной мощности.</span><span class="sxs-lookup"><span data-stu-id="ae8d2-123">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae8d2-124">-Тег</span><span class="sxs-lookup"><span data-stu-id="ae8d2-124">-Tag</span></span>
<span data-ttu-id="ae8d2-125">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов в пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="ae8d2-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae8d2-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae8d2-126">-Confirm</span></span>
<span data-ttu-id="ae8d2-127">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="ae8d2-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="ae8d2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae8d2-128">-WhatIf</span></span>
<span data-ttu-id="ae8d2-129">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="ae8d2-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="ae8d2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae8d2-130">CommonParameters</span></span>
<span data-ttu-id="ae8d2-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae8d2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae8d2-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae8d2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae8d2-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae8d2-133">INPUTS</span></span>

### <span data-ttu-id="ae8d2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ae8d2-134">System.String</span></span>

### <span data-ttu-id="ae8d2-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="ae8d2-135">System.String[]</span></span>

### <span data-ttu-id="ae8d2-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ae8d2-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ae8d2-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae8d2-137">OUTPUTS</span></span>

### <span data-ttu-id="ae8d2-138">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="ae8d2-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="ae8d2-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae8d2-139">NOTES</span></span>

## <span data-ttu-id="ae8d2-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae8d2-140">RELATED LINKS</span></span>

[<span data-ttu-id="ae8d2-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="ae8d2-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="ae8d2-142">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="ae8d2-142">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
