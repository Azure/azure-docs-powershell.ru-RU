---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
ms.openlocfilehash: c24f8f9e95db65b464da6586d9e3499358fc3edd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568580"
---
# <span data-ttu-id="3ccbb-101">New-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="3ccbb-101">New-AzureRmIotHub</span></span>

## <span data-ttu-id="3ccbb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ccbb-102">SYNOPSIS</span></span>
<span data-ttu-id="3ccbb-103">Создание нового IotHub.</span><span class="sxs-lookup"><span data-stu-id="3ccbb-103">Creates a new IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ccbb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ccbb-104">SYNTAX</span></span>

```
New-AzureRmIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ccbb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ccbb-105">DESCRIPTION</span></span>
<span data-ttu-id="3ccbb-106">Создание нового IotHub.</span><span class="sxs-lookup"><span data-stu-id="3ccbb-106">Creates a new IotHub.</span></span>
<span data-ttu-id="3ccbb-107">Вы можете создать IotHub с помощью свойств по умолчанию или указать Proerties ввода.</span><span class="sxs-lookup"><span data-stu-id="3ccbb-107">You can create the IotHub with either the default properties or specify the input proerties.</span></span>

## <span data-ttu-id="3ccbb-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ccbb-108">EXAMPLES</span></span>

### <span data-ttu-id="3ccbb-109">Пример 1. Создание нового IotHub со свойствами по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3ccbb-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="3ccbb-110">Создает новый IotHub с именем "myiothub" SKU "S1", емкость 1 и расположение "northeurope".</span><span class="sxs-lookup"><span data-stu-id="3ccbb-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="3ccbb-111">Пример 2. Создание нового IotHub с MaxDeliveryCount в очереди CloudtoDevice, равной 20</span><span class="sxs-lookup"><span data-stu-id="3ccbb-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudtoDevice Queue set to 20</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="3ccbb-112">Создает новый IotHub с именем "myiothub" SKU "S1", емкость 1 и расположение "northeurope" с расширенными свойствами ввода, представленными $properties.</span><span class="sxs-lookup"><span data-stu-id="3ccbb-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>

<span data-ttu-id="3ccbb-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. Commands. MaxDeliveryCount. IotHub. Models. PSCloudToDeviceProperties-Property @ {= 20} $properties = New-Object Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubInputProperties-Property @ {CloudToDevice = $psCloudToDeviceProperties} New-AzureRmIotHub-ResourceGroupName "myresourcegroup"-Names 1-myiothub</span><span class="sxs-lookup"><span data-stu-id="3ccbb-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="3ccbb-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ccbb-114">PARAMETERS</span></span>

### <span data-ttu-id="3ccbb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ccbb-115">-DefaultProfile</span></span>
<span data-ttu-id="3ccbb-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3ccbb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ccbb-117">-Location</span><span class="sxs-lookup"><span data-stu-id="3ccbb-117">-Location</span></span>
<span data-ttu-id="3ccbb-118">Расположение, в котором необходимо создать центр Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="3ccbb-118">Location where the IoT hub needs to be created.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ccbb-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3ccbb-119">-Name</span></span>
<span data-ttu-id="3ccbb-120">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="3ccbb-120">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ccbb-121">-Свойства</span><span class="sxs-lookup"><span data-stu-id="3ccbb-121">-Properties</span></span>
<span data-ttu-id="3ccbb-122">Свойства центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="3ccbb-122">Properties of the IoT hub.</span></span> 

```yaml
Type: PSIotHubInputProperties
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ccbb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ccbb-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ccbb-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3ccbb-124">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ccbb-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3ccbb-125">-SkuName</span></span>
<span data-ttu-id="3ccbb-126">Название SKU</span><span class="sxs-lookup"><span data-stu-id="3ccbb-126">Name of the sku</span></span>

```yaml
Type: PSIotHubSku
Parameter Sets: (All)
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ccbb-127">-Units</span><span class="sxs-lookup"><span data-stu-id="3ccbb-127">-Units</span></span>
<span data-ttu-id="3ccbb-128">Количество единиц</span><span class="sxs-lookup"><span data-stu-id="3ccbb-128">Number of units</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ccbb-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ccbb-129">-Confirm</span></span>
<span data-ttu-id="3ccbb-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3ccbb-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ccbb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ccbb-131">-WhatIf</span></span>
<span data-ttu-id="3ccbb-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3ccbb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ccbb-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3ccbb-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ccbb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ccbb-134">CommonParameters</span></span>
<span data-ttu-id="3ccbb-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ccbb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ccbb-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ccbb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ccbb-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ccbb-137">INPUTS</span></span>

### <span data-ttu-id="3ccbb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3ccbb-138">System.String</span></span>
<span data-ttu-id="3ccbb-139">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubSku System. Int64 Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubInputProperties</span><span class="sxs-lookup"><span data-stu-id="3ccbb-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku System.Int64 Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties</span></span>

## <span data-ttu-id="3ccbb-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ccbb-140">OUTPUTS</span></span>

### <span data-ttu-id="3ccbb-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3ccbb-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="3ccbb-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ccbb-142">NOTES</span></span>

## <span data-ttu-id="3ccbb-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ccbb-143">RELATED LINKS</span></span>

