---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: 392f9362df1cafdb6c047020b3381a7b16320607
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518398"
---
# <span data-ttu-id="82229-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="82229-101">New-AzIotHub</span></span>

## <span data-ttu-id="82229-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82229-102">SYNOPSIS</span></span>
<span data-ttu-id="82229-103">Создание нового IotHub.</span><span class="sxs-lookup"><span data-stu-id="82229-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="82229-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="82229-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82229-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82229-105">DESCRIPTION</span></span>
<span data-ttu-id="82229-106">Создание нового IotHub.</span><span class="sxs-lookup"><span data-stu-id="82229-106">Creates a new IotHub.</span></span>
<span data-ttu-id="82229-107">Вы можете создать IotHub со свойствами по умолчанию или указать входные свойства.</span><span class="sxs-lookup"><span data-stu-id="82229-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="82229-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="82229-108">EXAMPLES</span></span>

### <span data-ttu-id="82229-109">Пример 1. Создание нового IotHub со свойствами по умолчанию</span><span class="sxs-lookup"><span data-stu-id="82229-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Tag $tags
```

<span data-ttu-id="82229-110">Создает новый IotHub под названием "myiothub" SKU "S1", емкость 1 и расположение "northeurope", включаемого в теги.</span><span class="sxs-lookup"><span data-stu-id="82229-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" included with Tags.</span></span>

### <span data-ttu-id="82229-111">Пример 2. Создание нового IotHub с переменной MaxDeliveryCount в очереди CloudToDevice, которая имеет 20</span><span class="sxs-lookup"><span data-stu-id="82229-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="82229-112">Создает новый IotHub под названием "myiothub" SKU "S1", мощность 1 и расположение "northeurope" с расширенными свойствами ввода, представленными $properties.</span><span class="sxs-lookup"><span data-stu-id="82229-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="82229-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span><span class="sxs-lookup"><span data-stu-id="82229-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="82229-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82229-114">PARAMETERS</span></span>

### <span data-ttu-id="82229-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82229-115">-DefaultProfile</span></span>
<span data-ttu-id="82229-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="82229-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82229-117">-Location</span><span class="sxs-lookup"><span data-stu-id="82229-117">-Location</span></span>
<span data-ttu-id="82229-118">Расположение, в котором необходимо создать концентратор IoT.</span><span class="sxs-lookup"><span data-stu-id="82229-118">Location where the IoT hub needs to be created.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82229-119">-Name</span><span class="sxs-lookup"><span data-stu-id="82229-119">-Name</span></span>
<span data-ttu-id="82229-120">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="82229-120">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82229-121">-Properties</span><span class="sxs-lookup"><span data-stu-id="82229-121">-Properties</span></span>
<span data-ttu-id="82229-122">Свойства концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="82229-122">Properties of the IoT hub.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82229-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82229-123">-ResourceGroupName</span></span>
<span data-ttu-id="82229-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="82229-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82229-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="82229-125">-SkuName</span></span>
<span data-ttu-id="82229-126">Имя SKU</span><span class="sxs-lookup"><span data-stu-id="82229-126">Name of the sku</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: (All)
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82229-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="82229-127">-Tag</span></span>
<span data-ttu-id="82229-128">Теги экземпляров концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="82229-128">IoT hub instance tags.</span></span> <span data-ttu-id="82229-129">Пакет свойств в парах значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="82229-129">Property bag in key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="82229-130">-Units</span><span class="sxs-lookup"><span data-stu-id="82229-130">-Units</span></span>
<span data-ttu-id="82229-131">Количество единиц</span><span class="sxs-lookup"><span data-stu-id="82229-131">Number of units</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82229-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82229-132">-Confirm</span></span>
<span data-ttu-id="82229-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="82229-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82229-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82229-134">-WhatIf</span></span>
<span data-ttu-id="82229-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82229-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82229-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="82229-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82229-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82229-137">CommonParameters</span></span>
<span data-ttu-id="82229-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82229-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82229-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82229-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82229-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82229-140">INPUTS</span></span>

### <span data-ttu-id="82229-141">System.String</span><span class="sxs-lookup"><span data-stu-id="82229-141">System.String</span></span>

## <span data-ttu-id="82229-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="82229-142">OUTPUTS</span></span>

### <span data-ttu-id="82229-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="82229-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="82229-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="82229-144">NOTES</span></span>

## <span data-ttu-id="82229-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82229-145">RELATED LINKS</span></span>
