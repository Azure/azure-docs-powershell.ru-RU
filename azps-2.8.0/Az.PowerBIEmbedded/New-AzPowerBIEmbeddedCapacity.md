---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 3f2515a1c1039dbf9ff4a0635111c95a610d9834
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904514"
---
# <span data-ttu-id="3e4ba-101">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3e4ba-101">New-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3e4ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e4ba-102">SYNOPSIS</span></span>
<span data-ttu-id="3e4ba-103">Создает новую внедренную емкость PowerBI.</span><span class="sxs-lookup"><span data-stu-id="3e4ba-103">Creates a new PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="3e4ba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e4ba-104">SYNTAX</span></span>

```
New-AzPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e4ba-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e4ba-105">DESCRIPTION</span></span>
<span data-ttu-id="3e4ba-106">Командлет New-AzPowerBIEmbeddedCapacity создает новую пропускную способность PowerBI Embedded.</span><span class="sxs-lookup"><span data-stu-id="3e4ba-106">The New-AzPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="3e4ba-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e4ba-107">EXAMPLES</span></span>

### <span data-ttu-id="3e4ba-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3e4ba-108">Example 1</span></span>
```
PS C:\> New-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
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

<span data-ttu-id="3e4ba-109">Создает емкость с именем testcapacity в области "Центральная часть США и в группе ресурсов" в Azure Region testRG.</span><span class="sxs-lookup"><span data-stu-id="3e4ba-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="3e4ba-110">Уровень SKU для производственной мощности будет равен a1.</span><span class="sxs-lookup"><span data-stu-id="3e4ba-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="3e4ba-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e4ba-111">PARAMETERS</span></span>

### <span data-ttu-id="3e4ba-112">-Администратор</span><span class="sxs-lookup"><span data-stu-id="3e4ba-112">-Administrator</span></span>
<span data-ttu-id="3e4ba-113">Имена, разделенные запятыми, которые нужно установить в качестве администратора емкости</span><span class="sxs-lookup"><span data-stu-id="3e4ba-113">A comma separated names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="3e4ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e4ba-114">-DefaultProfile</span></span>
<span data-ttu-id="3e4ba-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e4ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e4ba-116">-Location</span><span class="sxs-lookup"><span data-stu-id="3e4ba-116">-Location</span></span>
<span data-ttu-id="3e4ba-117">Регион Azure, на котором размещена емкость для PowerBI Embedded</span><span class="sxs-lookup"><span data-stu-id="3e4ba-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="3e4ba-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3e4ba-118">-Name</span></span>
<span data-ttu-id="3e4ba-119">Имя встроенной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="3e4ba-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="3e4ba-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e4ba-120">-ResourceGroupName</span></span>
<span data-ttu-id="3e4ba-121">Имя группы ресурсов Azure, к которой относится емкость</span><span class="sxs-lookup"><span data-stu-id="3e4ba-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="3e4ba-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="3e4ba-122">-Sku</span></span>
<span data-ttu-id="3e4ba-123">Название SKU для производственной мощности.</span><span class="sxs-lookup"><span data-stu-id="3e4ba-123">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="3e4ba-124">-Тег</span><span class="sxs-lookup"><span data-stu-id="3e4ba-124">-Tag</span></span>
<span data-ttu-id="3e4ba-125">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов в пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="3e4ba-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="3e4ba-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e4ba-126">-Confirm</span></span>
<span data-ttu-id="3e4ba-127">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="3e4ba-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="3e4ba-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e4ba-128">-WhatIf</span></span>
<span data-ttu-id="3e4ba-129">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="3e4ba-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="3e4ba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e4ba-130">CommonParameters</span></span>
<span data-ttu-id="3e4ba-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e4ba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e4ba-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e4ba-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e4ba-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e4ba-133">INPUTS</span></span>

### <span data-ttu-id="3e4ba-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3e4ba-134">System.String</span></span>

### <span data-ttu-id="3e4ba-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="3e4ba-135">System.String[]</span></span>

### <span data-ttu-id="3e4ba-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3e4ba-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3e4ba-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e4ba-137">OUTPUTS</span></span>

### <span data-ttu-id="3e4ba-138">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3e4ba-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3e4ba-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e4ba-139">NOTES</span></span>

## <span data-ttu-id="3e4ba-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e4ba-140">RELATED LINKS</span></span>

[<span data-ttu-id="3e4ba-141">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3e4ba-141">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="3e4ba-142">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3e4ba-142">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
