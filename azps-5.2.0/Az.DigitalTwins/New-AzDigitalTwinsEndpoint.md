---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6b2c51d21b40745d3dd4dd2db71604fa01a5a6cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402460"
---
# <span data-ttu-id="27597-101">New-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="27597-101">New-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="27597-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27597-102">SYNOPSIS</span></span>
<span data-ttu-id="27597-103">Создание или обновление конечной точки DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="27597-103">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="27597-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="27597-104">SYNTAX</span></span>

### <span data-ttu-id="27597-105">EventHub (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27597-105">EventHub (Default)</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -ConnectionStringPrimaryKey <String> -EndpointType <EndpointType> [-SubscriptionId <String>]
 [-ConnectionStringSecondaryKey <String>] [-DeadLetterSecret <String>]
 [-EndpointDescription <IDigitalTwinsEndpointResource>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="27597-106">EventGrid</span><span class="sxs-lookup"><span data-stu-id="27597-106">EventGrid</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -AccessKey1 <String> -EndpointType <EndpointType> -TopicEndpoint <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="27597-107">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27597-107">ServiceBus</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -EndpointType <EndpointType> -PrimaryConnectionString <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="27597-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27597-108">DESCRIPTION</span></span>
<span data-ttu-id="27597-109">Создание или обновление конечной точки DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="27597-109">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="27597-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="27597-110">EXAMPLES</span></span>

### <span data-ttu-id="27597-111">Пример 1. Создание azDigitalTwinsEndpoint для Ервутуба</span><span class="sxs-lookup"><span data-stu-id="27597-111">Example 1: Create an AzDigitalTwinsEndpoint for Eventhub</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventHubEndPoint  -EndpointType EventHub -ResourceGroupName youritemp -ResourceName youriDigitalTwins -connectionStringPrimaryKey 'Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=youriEventhubPolicy;SharedAccessKey=********;EntityPath=yourieventhub'

Name                  Type
----                  ----
youriEventHubEndPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="27597-112">Создание azDigitalTwinsEndpoint для Eventhub с помощью connectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="27597-112">Create an AzDigitalTwinsEndpoint for Eventhub by connectionStringPrimaryKey</span></span>

### <span data-ttu-id="27597-113">Пример 2. Создание azDigitalTwinsEndpoint для EventGrid</span><span class="sxs-lookup"><span data-stu-id="27597-113">Example 2: Create an AzDigitalTwinsEndpoint for EventGrid</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventGridPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -TopicEndpoint 'https://yourieventgrid.eastus-1.eventgrid.azure.net/api/events' -AccessKey1 'xxxxxxxxx='

Name                  Type
----                  ----
youriEventGridPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="27597-114">Создание azDigitalTwinsEndpoint для Eventhub по TopicEndpoint и accessKey1</span><span class="sxs-lookup"><span data-stu-id="27597-114">Create an AzDigitalTwinsEndpoint for Eventhub by TopicEndpoint and accessKey1</span></span>

### <span data-ttu-id="27597-115">Пример 3. Создание azDigitalTwinsEndpoint для ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27597-115">Example 3: Create an AzDigitalTwinsEndpoint for ServiceBus</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriServiceBusPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -PrimaryConnectionString "Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=******;SharedAccessKey=********;EntityPath=yourieventhub"

Name                  Type
----                  ----
youriServiceBusPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="27597-116">Создание AzDigitalTwinsEndpoint для ServicBus с помощью PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="27597-116">Create an AzDigitalTwinsEndpoint for ServicBus by PrimaryConnectionString</span></span>

## <span data-ttu-id="27597-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27597-117">PARAMETERS</span></span>

### <span data-ttu-id="27597-118">-AccessKey1</span><span class="sxs-lookup"><span data-stu-id="27597-118">-AccessKey1</span></span>
<span data-ttu-id="27597-119">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="27597-119">The subscription identifier.</span></span>

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

### <span data-ttu-id="27597-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27597-120">-AsJob</span></span>
<span data-ttu-id="27597-121">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="27597-121">Run the command as a job</span></span>

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

### <span data-ttu-id="27597-122">-ConnectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="27597-122">-ConnectionStringPrimaryKey</span></span>
<span data-ttu-id="27597-123">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="27597-123">The subscription identifier.</span></span>

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

### <span data-ttu-id="27597-124">-ConnectionStringSecondaryKey</span><span class="sxs-lookup"><span data-stu-id="27597-124">-ConnectionStringSecondaryKey</span></span>
<span data-ttu-id="27597-125">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="27597-125">The subscription identifier.</span></span>

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

### <span data-ttu-id="27597-126">-DeadLetterSecret</span><span class="sxs-lookup"><span data-stu-id="27597-126">-DeadLetterSecret</span></span>
<span data-ttu-id="27597-127">Немерявная секретная буква в хранилище.</span><span class="sxs-lookup"><span data-stu-id="27597-127">Dead letter storage secret.</span></span>
<span data-ttu-id="27597-128">Во время чтения он будет заме же читаем.</span><span class="sxs-lookup"><span data-stu-id="27597-128">Will be obfuscated during read.</span></span>

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

### <span data-ttu-id="27597-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27597-129">-DefaultProfile</span></span>
<span data-ttu-id="27597-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27597-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27597-131">-EndpointDescription</span><span class="sxs-lookup"><span data-stu-id="27597-131">-EndpointDescription</span></span>
<span data-ttu-id="27597-132">Ресурс конечной точки DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="27597-132">DigitalTwinsInstance endpoint resource.</span></span>
<span data-ttu-id="27597-133">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств ENDPOINTDESCRIPTION и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="27597-133">To construct, see NOTES section for ENDPOINTDESCRIPTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="27597-134">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="27597-134">-EndpointName</span></span>
<span data-ttu-id="27597-135">Имя ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="27597-135">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="27597-136">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="27597-136">-EndpointType</span></span>
<span data-ttu-id="27597-137">Тип конечной точки цифровых технологий</span><span class="sxs-lookup"><span data-stu-id="27597-137">The type of Digital Twins endpoint</span></span>

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

### <span data-ttu-id="27597-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="27597-138">-NoWait</span></span>
<span data-ttu-id="27597-139">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="27597-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="27597-140">-PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="27597-140">-PrimaryConnectionString</span></span>
<span data-ttu-id="27597-141">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="27597-141">The subscription identifier.</span></span>

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

### <span data-ttu-id="27597-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27597-142">-ResourceGroupName</span></span>
<span data-ttu-id="27597-143">Имя группы ресурсов, которая содержит digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="27597-143">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="27597-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="27597-144">-ResourceName</span></span>
<span data-ttu-id="27597-145">Имя digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="27597-145">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="27597-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27597-146">-SubscriptionId</span></span>
<span data-ttu-id="27597-147">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="27597-147">The subscription identifier.</span></span>

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

### <span data-ttu-id="27597-148">-TopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="27597-148">-TopicEndpoint</span></span>
<span data-ttu-id="27597-149">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="27597-149">The subscription identifier.</span></span>

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

### <span data-ttu-id="27597-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27597-150">-Confirm</span></span>
<span data-ttu-id="27597-151">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="27597-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27597-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27597-152">-WhatIf</span></span>
<span data-ttu-id="27597-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27597-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27597-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="27597-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27597-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27597-155">CommonParameters</span></span>
<span data-ttu-id="27597-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27597-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27597-157">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27597-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27597-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27597-158">INPUTS</span></span>

### <span data-ttu-id="27597-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="27597-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="27597-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="27597-160">OUTPUTS</span></span>

### <span data-ttu-id="27597-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="27597-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="27597-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="27597-162">NOTES</span></span>

<span data-ttu-id="27597-163">ALIASES</span><span class="sxs-lookup"><span data-stu-id="27597-163">ALIASES</span></span>

<span data-ttu-id="27597-164">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="27597-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="27597-165">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="27597-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="27597-166">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="27597-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="27597-167">ENDPOINTDESCRIPTION : ресурс конечной точки <IDigitalTwinsEndpointResource> DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="27597-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource>: DigitalTwinsInstance endpoint resource.</span></span>
  - <span data-ttu-id="27597-168">`EndpointType <EndpointType>`: Тип конечной точки DigitalАs</span><span class="sxs-lookup"><span data-stu-id="27597-168">`EndpointType <EndpointType>`: The type of Digital Twins endpoint</span></span>
  - <span data-ttu-id="27597-169">`[DeadLetterSecret <String>]`: секрет хранилища с письмами.</span><span class="sxs-lookup"><span data-stu-id="27597-169">`[DeadLetterSecret <String>]`: Dead letter storage secret.</span></span> <span data-ttu-id="27597-170">Во время чтения он будет заме же читаем.</span><span class="sxs-lookup"><span data-stu-id="27597-170">Will be obfuscated during read.</span></span>

## <span data-ttu-id="27597-171">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27597-171">RELATED LINKS</span></span>

