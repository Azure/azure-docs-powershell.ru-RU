---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: 9011adbbfc7d23c2b9737e315fbec6001428d53c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065887"
---
# <span data-ttu-id="a6a07-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="a6a07-101">Set-AzIotHub</span></span>

## <span data-ttu-id="a6a07-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6a07-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a07-103">Обновляет свойства IotHub.</span><span class="sxs-lookup"><span data-stu-id="a6a07-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="a6a07-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6a07-104">SYNTAX</span></span>

### <span data-ttu-id="a6a07-105">UpdateSku (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a6a07-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6a07-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="a6a07-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6a07-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="a6a07-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6a07-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="a6a07-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6a07-109">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="a6a07-109">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6a07-110">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="a6a07-110">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6a07-111">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="a6a07-111">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6a07-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6a07-112">DESCRIPTION</span></span>
<span data-ttu-id="a6a07-113">Обновляет свойства IotHub.</span><span class="sxs-lookup"><span data-stu-id="a6a07-113">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="a6a07-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6a07-114">EXAMPLES</span></span>

### <span data-ttu-id="a6a07-115">Пример 1. Обновите SKU</span><span class="sxs-lookup"><span data-stu-id="a6a07-115">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="a6a07-116">Обновите SKU на S1 и Units to 5 для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="a6a07-116">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="a6a07-117">Пример 2. Обновите свойства eventhub</span><span class="sxs-lookup"><span data-stu-id="a6a07-117">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="a6a07-118">Обновление времени хранения телеметрии в днях на 4 для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="a6a07-118">Update the retention time of telemetry in days to 4 for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="a6a07-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6a07-119">PARAMETERS</span></span>

### <span data-ttu-id="a6a07-120">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="a6a07-120">-CloudToDevice</span></span>
<span data-ttu-id="a6a07-121">Свойства очереди команд "облако для устройства".</span><span class="sxs-lookup"><span data-stu-id="a6a07-121">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a07-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6a07-122">-DefaultProfile</span></span>
<span data-ttu-id="a6a07-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a6a07-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6a07-124">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="a6a07-124">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="a6a07-125">Флаг, указывающий, следует ли включить уведомления для отправки файла.</span><span class="sxs-lookup"><span data-stu-id="a6a07-125">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: System.Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a07-126">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="a6a07-126">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="a6a07-127">Срок хранения в днях.</span><span class="sxs-lookup"><span data-stu-id="a6a07-127">Retention time in days.</span></span> 

```yaml
Type: System.Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a07-128">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="a6a07-128">-FallbackRoute</span></span>
<span data-ttu-id="a6a07-129">Резервный маршрут для маршрутизации</span><span class="sxs-lookup"><span data-stu-id="a6a07-129">Fallback Route for Routing</span></span>

```yaml
Type: Microsoft.Azure.Management.IotHub.Models.PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a07-130">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="a6a07-130">-FileUploadContainerName</span></span>
<span data-ttu-id="a6a07-131">Имя контейнера, в который нужно добавить файлы.</span><span class="sxs-lookup"><span data-stu-id="a6a07-131">The name of the container to upload the files to.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a07-132">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="a6a07-132">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="a6a07-133">Максимальное число доставок для уведомлений о передаче файла.</span><span class="sxs-lookup"><span data-stu-id="a6a07-133">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a07-134">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="a6a07-134">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="a6a07-135">Время жизни для сообщений в очереди уведомлений о передаче файла.</span><span class="sxs-lookup"><span data-stu-id="a6a07-135">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a07-136">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="a6a07-136">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="a6a07-137">Срок жизни для URI SAS, который был создан для отправки файла.</span><span class="sxs-lookup"><span data-stu-id="a6a07-137">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a07-138">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="a6a07-138">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="a6a07-139">Строка подключения к хранилищу, в которую нужно добавить файлы.</span><span class="sxs-lookup"><span data-stu-id="a6a07-139">The storage connection string to upload the files to.</span></span> 

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a07-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a6a07-140">-Name</span></span>
<span data-ttu-id="a6a07-141">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="a6a07-141">Name of the IotHub</span></span>

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

### <span data-ttu-id="a6a07-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6a07-142">-ResourceGroupName</span></span>
<span data-ttu-id="a6a07-143">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a6a07-143">Resource Group Name</span></span>

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

### <span data-ttu-id="a6a07-144">-Routes</span><span class="sxs-lookup"><span data-stu-id="a6a07-144">-Routes</span></span>
<span data-ttu-id="a6a07-145">Маршруты, добавляемые для маршрутизации</span><span class="sxs-lookup"><span data-stu-id="a6a07-145">Routes to be added for Routing</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]
Parameter Sets: UpdateRouteProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a07-146">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="a6a07-146">-RoutingProperties</span></span>
<span data-ttu-id="a6a07-147">Свойства маршрутизации для маршрутизации сообщений во внешние конечные точки</span><span class="sxs-lookup"><span data-stu-id="a6a07-147">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a07-148">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a6a07-148">-SkuName</span></span>
<span data-ttu-id="a6a07-149">Название SKU.</span><span class="sxs-lookup"><span data-stu-id="a6a07-149">Name of the Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: UpdateSku
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a07-150">-Units</span><span class="sxs-lookup"><span data-stu-id="a6a07-150">-Units</span></span>
<span data-ttu-id="a6a07-151">Количество единиц</span><span class="sxs-lookup"><span data-stu-id="a6a07-151">Number of Units</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateSku
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a07-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6a07-152">-Confirm</span></span>
<span data-ttu-id="a6a07-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a6a07-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6a07-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6a07-154">-WhatIf</span></span>
<span data-ttu-id="a6a07-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a6a07-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6a07-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a6a07-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6a07-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a07-157">CommonParameters</span></span>
<span data-ttu-id="a6a07-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6a07-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a07-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6a07-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a07-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6a07-160">INPUTS</span></span>

### <span data-ttu-id="a6a07-161">System. String</span><span class="sxs-lookup"><span data-stu-id="a6a07-161">System.String</span></span>

## <span data-ttu-id="a6a07-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6a07-162">OUTPUTS</span></span>

### <span data-ttu-id="a6a07-163">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a6a07-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="a6a07-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6a07-164">NOTES</span></span>

## <span data-ttu-id="a6a07-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6a07-165">RELATED LINKS</span></span>
