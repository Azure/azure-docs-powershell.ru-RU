---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: dd0dfb633fd48f2f747d6f4c0eb3471745b40da1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517382"
---
# <span data-ttu-id="f7acb-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="f7acb-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="f7acb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7acb-102">SYNOPSIS</span></span>
<span data-ttu-id="f7acb-103">Удаляет подписку на раздел из указанного пространства имен автобусов обслуживания.</span><span class="sxs-lookup"><span data-stu-id="f7acb-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f7acb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f7acb-104">SYNTAX</span></span>

### <span data-ttu-id="f7acb-105">SubscriptionPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f7acb-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7acb-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f7acb-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7acb-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f7acb-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7acb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7acb-108">DESCRIPTION</span></span>
<span data-ttu-id="f7acb-109">Для **удаления подписки из** указанного пространства имен «Автобус обслуживания».</span><span class="sxs-lookup"><span data-stu-id="f7acb-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f7acb-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f7acb-110">EXAMPLES</span></span>

### <span data-ttu-id="f7acb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f7acb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="f7acb-112">Удаляет подписку на раздел, указанный в указанном пространстве имен `SB-TopicSubscription-Example1` `SB-Topic_exampl1` автобусов `SB-Example1` обслуживания.</span><span class="sxs-lookup"><span data-stu-id="f7acb-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="f7acb-113">Пример 2. InputObject — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="f7acb-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="f7acb-114">Пример 3. InputObject — использование piping:</span><span class="sxs-lookup"><span data-stu-id="f7acb-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="f7acb-115">Пример 4. ResourceId — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="f7acb-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="f7acb-116">Пример 5. ResourceId — использование строки:</span><span class="sxs-lookup"><span data-stu-id="f7acb-116">Example 5: ResourceId - Using string value:</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="f7acb-117">Удаляет подписку, предоставленную с ARM в параметре $resourceid/string для -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f7acb-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="f7acb-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7acb-118">PARAMETERS</span></span>

### <span data-ttu-id="f7acb-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7acb-119">-AsJob</span></span>
<span data-ttu-id="f7acb-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f7acb-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7acb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7acb-121">-DefaultProfile</span></span>
<span data-ttu-id="f7acb-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7acb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7acb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7acb-123">-InputObject</span></span>
<span data-ttu-id="f7acb-124">Service Bus Subscription Object</span><span class="sxs-lookup"><span data-stu-id="f7acb-124">Service Bus Subscription Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: SubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7acb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f7acb-125">-Name</span></span>
<span data-ttu-id="f7acb-126">Название подписки</span><span class="sxs-lookup"><span data-stu-id="f7acb-126">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7acb-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f7acb-127">-Namespace</span></span>
<span data-ttu-id="f7acb-128">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="f7acb-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7acb-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7acb-129">-PassThru</span></span>
<span data-ttu-id="f7acb-130">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="f7acb-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f7acb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7acb-131">-ResourceGroupName</span></span>
<span data-ttu-id="f7acb-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f7acb-132">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7acb-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7acb-133">-ResourceId</span></span>
<span data-ttu-id="f7acb-134">Service Bus Subscription Resource Id</span><span class="sxs-lookup"><span data-stu-id="f7acb-134">Service Bus Subscription Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7acb-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="f7acb-135">-Topic</span></span>
<span data-ttu-id="f7acb-136">Название темы</span><span class="sxs-lookup"><span data-stu-id="f7acb-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7acb-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7acb-137">-Confirm</span></span>
<span data-ttu-id="f7acb-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f7acb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7acb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7acb-139">-WhatIf</span></span>
<span data-ttu-id="f7acb-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7acb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7acb-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f7acb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7acb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7acb-142">CommonParameters</span></span>
<span data-ttu-id="f7acb-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7acb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7acb-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7acb-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7acb-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7acb-145">INPUTS</span></span>

### <span data-ttu-id="f7acb-146">System.String</span><span class="sxs-lookup"><span data-stu-id="f7acb-146">System.String</span></span>

### <span data-ttu-id="f7acb-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="f7acb-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="f7acb-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f7acb-148">OUTPUTS</span></span>

### <span data-ttu-id="f7acb-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f7acb-149">System.Boolean</span></span>

## <span data-ttu-id="f7acb-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f7acb-150">NOTES</span></span>

## <span data-ttu-id="f7acb-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7acb-151">RELATED LINKS</span></span>
