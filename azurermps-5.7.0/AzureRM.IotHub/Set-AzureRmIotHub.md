---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/set-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
ms.openlocfilehash: a9005819bb78e5393f3a617dd18886309d3defc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735005"
---
# <span data-ttu-id="8022c-101">Set-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="8022c-101">Set-AzureRmIotHub</span></span>

## <span data-ttu-id="8022c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8022c-102">SYNOPSIS</span></span>
<span data-ttu-id="8022c-103">Обновляет свойства IotHub.</span><span class="sxs-lookup"><span data-stu-id="8022c-103">Updates the properties of an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8022c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8022c-104">SYNTAX</span></span>

### <span data-ttu-id="8022c-105">UpdateSku (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8022c-105">UpdateSku (Default)</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8022c-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="8022c-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8022c-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="8022c-107">UpdateFileUploadProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8022c-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="8022c-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8022c-109">UpdateOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="8022c-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8022c-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="8022c-110">UpdateRoutingProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8022c-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="8022c-111">UpdateRouteProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8022c-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="8022c-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8022c-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8022c-113">DESCRIPTION</span></span>
<span data-ttu-id="8022c-114">Обновляет свойства IotHub.</span><span class="sxs-lookup"><span data-stu-id="8022c-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="8022c-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8022c-115">EXAMPLES</span></span>

### <span data-ttu-id="8022c-116">Пример 1. Обновите SKU</span><span class="sxs-lookup"><span data-stu-id="8022c-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="8022c-117">Обновите SKU на S1 и Units to 5 для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="8022c-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="8022c-118">Пример 2. Обновите свойства eventhub</span><span class="sxs-lookup"><span data-stu-id="8022c-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="8022c-119">Обновление времени хранения в днях на 4 для событий телеметрии и operationsmonitoringevents для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="8022c-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="8022c-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8022c-120">PARAMETERS</span></span>

### <span data-ttu-id="8022c-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="8022c-121">-CloudToDevice</span></span>
<span data-ttu-id="8022c-122">Свойства очереди команд "облако для устройства".</span><span class="sxs-lookup"><span data-stu-id="8022c-122">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8022c-123">-DefaultProfile</span></span>
<span data-ttu-id="8022c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8022c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8022c-125">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="8022c-125">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="8022c-126">Флаг, указывающий, следует ли включить уведомления для отправки файла.</span><span class="sxs-lookup"><span data-stu-id="8022c-126">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-127">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="8022c-127">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="8022c-128">Срок хранения в днях.</span><span class="sxs-lookup"><span data-stu-id="8022c-128">Retention time in days.</span></span> 

```yaml
Type: Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-129">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="8022c-129">-FallbackRoute</span></span>
<span data-ttu-id="8022c-130">Резервный маршрут для маршрутизации</span><span class="sxs-lookup"><span data-stu-id="8022c-130">Fallback Route for Routing</span></span>

```yaml
Type: PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-131">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="8022c-131">-FileUploadContainerName</span></span>
<span data-ttu-id="8022c-132">Имя контейнера, в который нужно добавить файлы.</span><span class="sxs-lookup"><span data-stu-id="8022c-132">The name of the container to upload the files to.</span></span>

```yaml
Type: String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-133">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="8022c-133">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="8022c-134">Максимальное число доставок для уведомлений о передаче файла.</span><span class="sxs-lookup"><span data-stu-id="8022c-134">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: Int32
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-135">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="8022c-135">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="8022c-136">Время жизни для сообщений в очереди уведомлений о передаче файла.</span><span class="sxs-lookup"><span data-stu-id="8022c-136">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-137">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="8022c-137">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="8022c-138">Срок жизни для URI SAS, который был создан для отправки файла.</span><span class="sxs-lookup"><span data-stu-id="8022c-138">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-139">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="8022c-139">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="8022c-140">Строка подключения к хранилищу, в которую нужно добавить файлы.</span><span class="sxs-lookup"><span data-stu-id="8022c-140">The storage connection string to upload the files to.</span></span> 

```yaml
Type: String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8022c-141">-Name</span></span>
<span data-ttu-id="8022c-142">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="8022c-142">Name of the IotHub</span></span>

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

### <span data-ttu-id="8022c-143">-OperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="8022c-143">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="8022c-144">Свойства, связанные с мониторингом операций.</span><span class="sxs-lookup"><span data-stu-id="8022c-144">The properties related to operations monitoring.</span></span> 

```yaml
Type: PSOperationsMonitoringProperties
Parameter Sets: UpdateOperationsMonitoringProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8022c-145">-ResourceGroupName</span></span>
<span data-ttu-id="8022c-146">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8022c-146">Resource Group Name</span></span>

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

### <span data-ttu-id="8022c-147">-Routes</span><span class="sxs-lookup"><span data-stu-id="8022c-147">-Routes</span></span>
<span data-ttu-id="8022c-148">Маршруты, добавляемые для маршрутизации</span><span class="sxs-lookup"><span data-stu-id="8022c-148">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="8022c-149">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="8022c-149">-RoutingProperties</span></span>
<span data-ttu-id="8022c-150">Свойства маршрутизации для маршрутизации сообщений во внешние конечные точки</span><span class="sxs-lookup"><span data-stu-id="8022c-150">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-151">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8022c-151">-SkuName</span></span>
<span data-ttu-id="8022c-152">Название SKU.</span><span class="sxs-lookup"><span data-stu-id="8022c-152">Name of the Sku.</span></span>

```yaml
Type: PSIotHubSku
Parameter Sets: UpdateSku
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-153">-Units</span><span class="sxs-lookup"><span data-stu-id="8022c-153">-Units</span></span>
<span data-ttu-id="8022c-154">Количество единиц</span><span class="sxs-lookup"><span data-stu-id="8022c-154">Number of Units</span></span>

```yaml
Type: Int64
Parameter Sets: UpdateSku
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8022c-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8022c-155">-Confirm</span></span>
<span data-ttu-id="8022c-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8022c-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8022c-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8022c-157">-WhatIf</span></span>
<span data-ttu-id="8022c-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8022c-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8022c-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8022c-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8022c-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8022c-160">CommonParameters</span></span>
<span data-ttu-id="8022c-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8022c-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8022c-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8022c-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8022c-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8022c-163">INPUTS</span></span>

### <span data-ttu-id="8022c-164">System. String</span><span class="sxs-lookup"><span data-stu-id="8022c-164">System.String</span></span>
<span data-ttu-id="8022c-165">Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceProperties Microsoft. Azure. Commands. Management. IotHub. Models. PSOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="8022c-165">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties</span></span>

## <span data-ttu-id="8022c-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8022c-166">OUTPUTS</span></span>

### <span data-ttu-id="8022c-167">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8022c-167">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="8022c-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="8022c-168">NOTES</span></span>

## <span data-ttu-id="8022c-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8022c-169">RELATED LINKS</span></span>

