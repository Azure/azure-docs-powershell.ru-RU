---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6b2c51d21b40745d3dd4dd2db71604fa01a5a6cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504955"
---
# <span data-ttu-id="f92d5-101">New-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="f92d5-101">New-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="f92d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f92d5-102">SYNOPSIS</span></span>
<span data-ttu-id="f92d5-103">Создание или обновление конечной точки DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="f92d5-103">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="f92d5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f92d5-104">SYNTAX</span></span>

### <span data-ttu-id="f92d5-105">EventHub (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f92d5-105">EventHub (Default)</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -ConnectionStringPrimaryKey <String> -EndpointType <EndpointType> [-SubscriptionId <String>]
 [-ConnectionStringSecondaryKey <String>] [-DeadLetterSecret <String>]
 [-EndpointDescription <IDigitalTwinsEndpointResource>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f92d5-106">EventGrid</span><span class="sxs-lookup"><span data-stu-id="f92d5-106">EventGrid</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -AccessKey1 <String> -EndpointType <EndpointType> -TopicEndpoint <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f92d5-107">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f92d5-107">ServiceBus</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -EndpointType <EndpointType> -PrimaryConnectionString <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f92d5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f92d5-108">DESCRIPTION</span></span>
<span data-ttu-id="f92d5-109">Создание или обновление конечной точки DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="f92d5-109">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="f92d5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f92d5-110">EXAMPLES</span></span>

### <span data-ttu-id="f92d5-111">Пример 1. Создание azDigitalTwinsEndpoint для Ервутуба</span><span class="sxs-lookup"><span data-stu-id="f92d5-111">Example 1: Create an AzDigitalTwinsEndpoint for Eventhub</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventHubEndPoint  -EndpointType EventHub -ResourceGroupName youritemp -ResourceName youriDigitalTwins -connectionStringPrimaryKey 'Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=youriEventhubPolicy;SharedAccessKey=********;EntityPath=yourieventhub'

Name                  Type
----                  ----
youriEventHubEndPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="f92d5-112">Создание azDigitalTwinsEndpoint для Eventhub с помощью connectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="f92d5-112">Create an AzDigitalTwinsEndpoint for Eventhub by connectionStringPrimaryKey</span></span>

### <span data-ttu-id="f92d5-113">Пример 2. Создание azDigitalTwinsEndpoint для EventGrid</span><span class="sxs-lookup"><span data-stu-id="f92d5-113">Example 2: Create an AzDigitalTwinsEndpoint for EventGrid</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventGridPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -TopicEndpoint 'https://yourieventgrid.eastus-1.eventgrid.azure.net/api/events' -AccessKey1 'xxxxxxxxx='

Name                  Type
----                  ----
youriEventGridPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="f92d5-114">Создание azDigitalTwinsEndpoint для Eventhub по TopicEndpoint и accessKey1</span><span class="sxs-lookup"><span data-stu-id="f92d5-114">Create an AzDigitalTwinsEndpoint for Eventhub by TopicEndpoint and accessKey1</span></span>

### <span data-ttu-id="f92d5-115">Пример 3. Создание azDigitalTwinsEndpoint для ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f92d5-115">Example 3: Create an AzDigitalTwinsEndpoint for ServiceBus</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriServiceBusPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -PrimaryConnectionString "Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=******;SharedAccessKey=********;EntityPath=yourieventhub"

Name                  Type
----                  ----
youriServiceBusPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="f92d5-116">Создание AzDigitalTwinsEndpoint для ServicBus с помощью PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="f92d5-116">Create an AzDigitalTwinsEndpoint for ServicBus by PrimaryConnectionString</span></span>

## <span data-ttu-id="f92d5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f92d5-117">PARAMETERS</span></span>

### <span data-ttu-id="f92d5-118">-AccessKey1</span><span class="sxs-lookup"><span data-stu-id="f92d5-118">-AccessKey1</span></span>
<span data-ttu-id="f92d5-119">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="f92d5-119">The subscription identifier.</span></span>

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

### <span data-ttu-id="f92d5-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f92d5-120">-AsJob</span></span>
<span data-ttu-id="f92d5-121">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="f92d5-121">Run the command as a job</span></span>

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

### <span data-ttu-id="f92d5-122">-ConnectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="f92d5-122">-ConnectionStringPrimaryKey</span></span>
<span data-ttu-id="f92d5-123">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="f92d5-123">The subscription identifier.</span></span>

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

### <span data-ttu-id="f92d5-124">-ConnectionStringSecondaryKey</span><span class="sxs-lookup"><span data-stu-id="f92d5-124">-ConnectionStringSecondaryKey</span></span>
<span data-ttu-id="f92d5-125">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="f92d5-125">The subscription identifier.</span></span>

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

### <span data-ttu-id="f92d5-126">-DeadLetterSecret</span><span class="sxs-lookup"><span data-stu-id="f92d5-126">-DeadLetterSecret</span></span>
<span data-ttu-id="f92d5-127">Немерявная секретная буква в хранилище.</span><span class="sxs-lookup"><span data-stu-id="f92d5-127">Dead letter storage secret.</span></span>
<span data-ttu-id="f92d5-128">Во время чтения он будет заме же читаем.</span><span class="sxs-lookup"><span data-stu-id="f92d5-128">Will be obfuscated during read.</span></span>

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

### <span data-ttu-id="f92d5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f92d5-129">-DefaultProfile</span></span>
<span data-ttu-id="f92d5-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f92d5-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f92d5-131">-EndpointDescription</span><span class="sxs-lookup"><span data-stu-id="f92d5-131">-EndpointDescription</span></span>
<span data-ttu-id="f92d5-132">Ресурс конечной точки DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="f92d5-132">DigitalTwinsInstance endpoint resource.</span></span>
<span data-ttu-id="f92d5-133">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств ENDPOINTDESCRIPTION и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="f92d5-133">To construct, see NOTES section for ENDPOINTDESCRIPTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="f92d5-134">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f92d5-134">-EndpointName</span></span>
<span data-ttu-id="f92d5-135">Имя ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="f92d5-135">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="f92d5-136">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="f92d5-136">-EndpointType</span></span>
<span data-ttu-id="f92d5-137">Тип конечной точки цифровых технологий</span><span class="sxs-lookup"><span data-stu-id="f92d5-137">The type of Digital Twins endpoint</span></span>

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

### <span data-ttu-id="f92d5-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f92d5-138">-NoWait</span></span>
<span data-ttu-id="f92d5-139">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="f92d5-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f92d5-140">-PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="f92d5-140">-PrimaryConnectionString</span></span>
<span data-ttu-id="f92d5-141">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="f92d5-141">The subscription identifier.</span></span>

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

### <span data-ttu-id="f92d5-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f92d5-142">-ResourceGroupName</span></span>
<span data-ttu-id="f92d5-143">Имя группы ресурсов, которая содержит digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="f92d5-143">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="f92d5-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f92d5-144">-ResourceName</span></span>
<span data-ttu-id="f92d5-145">Имя digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="f92d5-145">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="f92d5-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f92d5-146">-SubscriptionId</span></span>
<span data-ttu-id="f92d5-147">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="f92d5-147">The subscription identifier.</span></span>

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

### <span data-ttu-id="f92d5-148">-TopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="f92d5-148">-TopicEndpoint</span></span>
<span data-ttu-id="f92d5-149">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="f92d5-149">The subscription identifier.</span></span>

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

### <span data-ttu-id="f92d5-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f92d5-150">-Confirm</span></span>
<span data-ttu-id="f92d5-151">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f92d5-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f92d5-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f92d5-152">-WhatIf</span></span>
<span data-ttu-id="f92d5-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f92d5-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f92d5-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f92d5-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f92d5-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f92d5-155">CommonParameters</span></span>
<span data-ttu-id="f92d5-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f92d5-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f92d5-157">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f92d5-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f92d5-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f92d5-158">INPUTS</span></span>

### <span data-ttu-id="f92d5-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="f92d5-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="f92d5-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f92d5-160">OUTPUTS</span></span>

### <span data-ttu-id="f92d5-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="f92d5-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="f92d5-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f92d5-162">NOTES</span></span>

<span data-ttu-id="f92d5-163">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f92d5-163">ALIASES</span></span>

<span data-ttu-id="f92d5-164">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="f92d5-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f92d5-165">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="f92d5-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f92d5-166">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f92d5-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f92d5-167">ENDPOINTDESCRIPTION : ресурс конечной точки <IDigitalTwinsEndpointResource> DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="f92d5-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource>: DigitalTwinsInstance endpoint resource.</span></span>
  - <span data-ttu-id="f92d5-168">`EndpointType <EndpointType>`: Тип конечной точки DigitalАs</span><span class="sxs-lookup"><span data-stu-id="f92d5-168">`EndpointType <EndpointType>`: The type of Digital Twins endpoint</span></span>
  - <span data-ttu-id="f92d5-169">`[DeadLetterSecret <String>]`: секрет хранилища с письмами.</span><span class="sxs-lookup"><span data-stu-id="f92d5-169">`[DeadLetterSecret <String>]`: Dead letter storage secret.</span></span> <span data-ttu-id="f92d5-170">Во время чтения он будет заме же читаем.</span><span class="sxs-lookup"><span data-stu-id="f92d5-170">Will be obfuscated during read.</span></span>

## <span data-ttu-id="f92d5-171">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f92d5-171">RELATED LINKS</span></span>

