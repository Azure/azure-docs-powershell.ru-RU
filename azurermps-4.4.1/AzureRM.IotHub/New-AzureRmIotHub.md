---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
ms.openlocfilehash: ad491605fcba26f713fcf295c419990e9db6ff2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734556"
---
# <span data-ttu-id="eb084-101">New-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="eb084-101">New-AzureRmIotHub</span></span>

## <span data-ttu-id="eb084-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb084-102">SYNOPSIS</span></span>
<span data-ttu-id="eb084-103">Создание нового IotHub.</span><span class="sxs-lookup"><span data-stu-id="eb084-103">Creates a new IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb084-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb084-104">SYNTAX</span></span>

```
New-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <PSIotHubSku> [-Units] <Int64>
 [-Location] <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb084-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb084-105">DESCRIPTION</span></span>
<span data-ttu-id="eb084-106">Создание нового IotHub.</span><span class="sxs-lookup"><span data-stu-id="eb084-106">Creates a new IotHub.</span></span>
<span data-ttu-id="eb084-107">Вы можете создать IotHub с помощью свойств по умолчанию или указать Proerties ввода.</span><span class="sxs-lookup"><span data-stu-id="eb084-107">You can create the IotHub with either the default properties or specify the input proerties.</span></span>

## <span data-ttu-id="eb084-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb084-108">EXAMPLES</span></span>

### <span data-ttu-id="eb084-109">Пример 1. Создание нового IotHub со свойствами по умолчанию</span><span class="sxs-lookup"><span data-stu-id="eb084-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="eb084-110">Создает новый IotHub с именем "myiothub" SKU "S1", емкость 1 и расположение "northeurope".</span><span class="sxs-lookup"><span data-stu-id="eb084-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="eb084-111">Пример 2. Создание нового IotHub с MaxDeliveryCount в очереди CloudtoDevice, равной 20</span><span class="sxs-lookup"><span data-stu-id="eb084-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudtoDevice Queue set to 20</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="eb084-112">Создает новый IotHub с именем "myiothub" SKU "S1", емкость 1 и расположение "northeurope" с расширенными свойствами ввода, представленными $properties.</span><span class="sxs-lookup"><span data-stu-id="eb084-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>

<span data-ttu-id="eb084-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. Commands. MaxDeliveryCount. IotHub. Models. PSCloudToDeviceProperties-Property @ {= 20} $properties = New-Object Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubInputProperties-Property @ {CloudToDevice = $psCloudToDeviceProperties} New-AzureRmIotHub-ResourceGroupName "myresourcegroup"-Names 1-myiothub</span><span class="sxs-lookup"><span data-stu-id="eb084-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="eb084-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb084-114">PARAMETERS</span></span>

### <span data-ttu-id="eb084-115">-Location</span><span class="sxs-lookup"><span data-stu-id="eb084-115">-Location</span></span>
<span data-ttu-id="eb084-116">Расположение, в котором необходимо создать центр Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="eb084-116">Location where the IoT hub needs to be created.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb084-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eb084-117">-Name</span></span>
<span data-ttu-id="eb084-118">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="eb084-118">Name of the IotHub</span></span>

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

### <span data-ttu-id="eb084-119">-Свойства</span><span class="sxs-lookup"><span data-stu-id="eb084-119">-Properties</span></span>
<span data-ttu-id="eb084-120">Свойства центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="eb084-120">Properties of the IoT hub.</span></span> 

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

### <span data-ttu-id="eb084-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb084-121">-ResourceGroupName</span></span>
<span data-ttu-id="eb084-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="eb084-122">Resource Group Name</span></span>

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

### <span data-ttu-id="eb084-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="eb084-123">-SkuName</span></span>
<span data-ttu-id="eb084-124">Название SKU</span><span class="sxs-lookup"><span data-stu-id="eb084-124">Name of the sku</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: (All)
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb084-125">-Units</span><span class="sxs-lookup"><span data-stu-id="eb084-125">-Units</span></span>
<span data-ttu-id="eb084-126">Количество единиц</span><span class="sxs-lookup"><span data-stu-id="eb084-126">Number of units</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb084-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb084-127">-Confirm</span></span>
<span data-ttu-id="eb084-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eb084-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb084-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb084-129">-WhatIf</span></span>
<span data-ttu-id="eb084-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eb084-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb084-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eb084-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb084-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb084-132">-DefaultProfile</span></span>
<span data-ttu-id="eb084-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb084-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb084-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb084-134">CommonParameters</span></span>
<span data-ttu-id="eb084-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb084-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb084-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb084-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb084-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb084-137">INPUTS</span></span>

### <span data-ttu-id="eb084-138">System. String</span><span class="sxs-lookup"><span data-stu-id="eb084-138">System.String</span></span>
<span data-ttu-id="eb084-139">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubSku System. Int64 Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubInputProperties</span><span class="sxs-lookup"><span data-stu-id="eb084-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku System.Int64 Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties</span></span>

## <span data-ttu-id="eb084-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb084-140">OUTPUTS</span></span>

### <span data-ttu-id="eb084-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="eb084-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="eb084-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb084-142">NOTES</span></span>

## <span data-ttu-id="eb084-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb084-143">RELATED LINKS</span></span>

