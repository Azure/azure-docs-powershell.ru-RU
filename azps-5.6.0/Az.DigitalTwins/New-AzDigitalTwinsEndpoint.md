---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/new-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 3c59099a2e4440e2c92836ab02b8396b5fc3b207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984945"
---
# <span data-ttu-id="d84ec-101">New-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="d84ec-101">New-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="d84ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d84ec-102">SYNOPSIS</span></span>
<span data-ttu-id="d84ec-103">Создание или обновление конечной точки DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="d84ec-103">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="d84ec-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d84ec-104">SYNTAX</span></span>

### <span data-ttu-id="d84ec-105">EventHub (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d84ec-105">EventHub (Default)</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -ConnectionStringPrimaryKey <String> -EndpointType <EndpointType> [-SubscriptionId <String>]
 [-ConnectionStringSecondaryKey <String>] [-DeadLetterSecret <String>]
 [-EndpointDescription <IDigitalTwinsEndpointResource>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d84ec-106">EventGrid</span><span class="sxs-lookup"><span data-stu-id="d84ec-106">EventGrid</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -AccessKey1 <String> -EndpointType <EndpointType> -TopicEndpoint <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d84ec-107">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d84ec-107">ServiceBus</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -EndpointType <EndpointType> -PrimaryConnectionString <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d84ec-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d84ec-108">DESCRIPTION</span></span>
<span data-ttu-id="d84ec-109">Создание или обновление конечной точки DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="d84ec-109">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="d84ec-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d84ec-110">EXAMPLES</span></span>

### <span data-ttu-id="d84ec-111">Пример 1. Создание azDigitalTwinsEndpoint для Ервутуба</span><span class="sxs-lookup"><span data-stu-id="d84ec-111">Example 1: Create an AzDigitalTwinsEndpoint for Eventhub</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventHubEndPoint  -EndpointType EventHub -ResourceGroupName youritemp -ResourceName youriDigitalTwins -connectionStringPrimaryKey 'Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=youriEventhubPolicy;SharedAccessKey=********;EntityPath=yourieventhub'

Name                  Type
----                  ----
youriEventHubEndPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="d84ec-112">Создание azDigitalTwinsEndpoint для Eventhub с помощью connectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="d84ec-112">Create an AzDigitalTwinsEndpoint for Eventhub by connectionStringPrimaryKey</span></span>

### <span data-ttu-id="d84ec-113">Пример 2. Создание azDigitalTwinsEndpoint для EventGrid</span><span class="sxs-lookup"><span data-stu-id="d84ec-113">Example 2: Create an AzDigitalTwinsEndpoint for EventGrid</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventGridPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -TopicEndpoint 'https://yourieventgrid.eastus-1.eventgrid.azure.net/api/events' -AccessKey1 'xxxxxxxxx='

Name                  Type
----                  ----
youriEventGridPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="d84ec-114">Создание azDigitalTwinsEndpoint для Eventhub по TopicEndpoint и accessKey1</span><span class="sxs-lookup"><span data-stu-id="d84ec-114">Create an AzDigitalTwinsEndpoint for Eventhub by TopicEndpoint and accessKey1</span></span>

### <span data-ttu-id="d84ec-115">Пример 3. Создание azDigitalTwinsEndpoint для ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d84ec-115">Example 3: Create an AzDigitalTwinsEndpoint for ServiceBus</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriServiceBusPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -PrimaryConnectionString "Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=******;SharedAccessKey=********;EntityPath=yourieventhub"

Name                  Type
----                  ----
youriServiceBusPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="d84ec-116">Создание AzDigitalTwinsEndpoint для ServicBus с помощью PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="d84ec-116">Create an AzDigitalTwinsEndpoint for ServicBus by PrimaryConnectionString</span></span>

## <span data-ttu-id="d84ec-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d84ec-117">PARAMETERS</span></span>

### <span data-ttu-id="d84ec-118">-AccessKey1</span><span class="sxs-lookup"><span data-stu-id="d84ec-118">-AccessKey1</span></span>
<span data-ttu-id="d84ec-119">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="d84ec-119">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ec-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d84ec-120">-AsJob</span></span>
<span data-ttu-id="d84ec-121">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="d84ec-121">Run the command as a job</span></span>

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

### <span data-ttu-id="d84ec-122">-ConnectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="d84ec-122">-ConnectionStringPrimaryKey</span></span>
<span data-ttu-id="d84ec-123">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="d84ec-123">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ec-124">-ConnectionStringSecondaryKey</span><span class="sxs-lookup"><span data-stu-id="d84ec-124">-ConnectionStringSecondaryKey</span></span>
<span data-ttu-id="d84ec-125">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="d84ec-125">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ec-126">-DeadLetterSecret</span><span class="sxs-lookup"><span data-stu-id="d84ec-126">-DeadLetterSecret</span></span>
<span data-ttu-id="d84ec-127">Секрет хранилища с письмами.</span><span class="sxs-lookup"><span data-stu-id="d84ec-127">Dead letter storage secret.</span></span>
<span data-ttu-id="d84ec-128">Во время чтения он будет заме же читаем.</span><span class="sxs-lookup"><span data-stu-id="d84ec-128">Will be obfuscated during read.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ec-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d84ec-129">-DefaultProfile</span></span>
<span data-ttu-id="d84ec-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d84ec-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ec-131">-EndpointDescription</span><span class="sxs-lookup"><span data-stu-id="d84ec-131">-EndpointDescription</span></span>
<span data-ttu-id="d84ec-132">Ресурс конечной точки DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="d84ec-132">DigitalTwinsInstance endpoint resource.</span></span>
<span data-ttu-id="d84ec-133">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств ENDPOINTDESCRIPTION и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="d84ec-133">To construct, see NOTES section for ENDPOINTDESCRIPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d84ec-134">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d84ec-134">-EndpointName</span></span>
<span data-ttu-id="d84ec-135">Имя ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d84ec-135">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="d84ec-136">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="d84ec-136">-EndpointType</span></span>
<span data-ttu-id="d84ec-137">Тип конечной точки цифровых технологий</span><span class="sxs-lookup"><span data-stu-id="d84ec-137">The type of Digital Twins endpoint</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Support.EndpointType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ec-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d84ec-138">-NoWait</span></span>
<span data-ttu-id="d84ec-139">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="d84ec-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d84ec-140">-PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="d84ec-140">-PrimaryConnectionString</span></span>
<span data-ttu-id="d84ec-141">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="d84ec-141">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceBus
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ec-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d84ec-142">-ResourceGroupName</span></span>
<span data-ttu-id="d84ec-143">Имя группы ресурсов, которая содержит digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="d84ec-143">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="d84ec-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d84ec-144">-ResourceName</span></span>
<span data-ttu-id="d84ec-145">Имя digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="d84ec-145">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="d84ec-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d84ec-146">-SubscriptionId</span></span>
<span data-ttu-id="d84ec-147">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="d84ec-147">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ec-148">-TopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="d84ec-148">-TopicEndpoint</span></span>
<span data-ttu-id="d84ec-149">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="d84ec-149">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ec-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d84ec-150">-Confirm</span></span>
<span data-ttu-id="d84ec-151">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d84ec-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d84ec-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d84ec-152">-WhatIf</span></span>
<span data-ttu-id="d84ec-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d84ec-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d84ec-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d84ec-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d84ec-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d84ec-155">CommonParameters</span></span>
<span data-ttu-id="d84ec-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d84ec-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d84ec-157">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d84ec-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d84ec-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d84ec-158">INPUTS</span></span>

### <span data-ttu-id="d84ec-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="d84ec-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="d84ec-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d84ec-160">OUTPUTS</span></span>

### <span data-ttu-id="d84ec-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="d84ec-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="d84ec-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d84ec-162">NOTES</span></span>

<span data-ttu-id="d84ec-163">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d84ec-163">ALIASES</span></span>

<span data-ttu-id="d84ec-164">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d84ec-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d84ec-165">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="d84ec-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d84ec-166">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d84ec-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d84ec-167">ENDPOINTDESCRIPTION : ресурс конечной точки <IDigitalTwinsEndpointResource> DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="d84ec-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource>: DigitalTwinsInstance endpoint resource.</span></span>
  - <span data-ttu-id="d84ec-168">`EndpointType <EndpointType>`: Тип конечной точки DigitalАs</span><span class="sxs-lookup"><span data-stu-id="d84ec-168">`EndpointType <EndpointType>`: The type of Digital Twins endpoint</span></span>
  - <span data-ttu-id="d84ec-169">`[DeadLetterSecret <String>]`— секрет хранилища с письмами.</span><span class="sxs-lookup"><span data-stu-id="d84ec-169">`[DeadLetterSecret <String>]`: Dead letter storage secret.</span></span> <span data-ttu-id="d84ec-170">Во время чтения он будет заме же читаем.</span><span class="sxs-lookup"><span data-stu-id="d84ec-170">Will be obfuscated during read.</span></span>

## <span data-ttu-id="d84ec-171">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d84ec-171">RELATED LINKS</span></span>

