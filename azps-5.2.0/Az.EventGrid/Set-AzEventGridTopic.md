---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: 6a6b373fcbe38aac7e4e8d3972206955942eb18e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412852"
---
# <span data-ttu-id="7e978-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="7e978-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="7e978-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e978-102">SYNOPSIS</span></span>
<span data-ttu-id="7e978-103">Задает свойства раздела сетки событий.</span><span class="sxs-lookup"><span data-stu-id="7e978-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="7e978-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7e978-104">SYNTAX</span></span>

### <span data-ttu-id="7e978-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7e978-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-InboundIpRule] <Hashtable> [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e978-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e978-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-InboundIpRule] <Hashtable>
 [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e978-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e978-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [[-InboundIpRule] <Hashtable>]
 [[-PublicNetworkAccess] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e978-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e978-108">DESCRIPTION</span></span>
<span data-ttu-id="7e978-109">Задает свойства раздела сетки событий.</span><span class="sxs-lookup"><span data-stu-id="7e978-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="7e978-110">Его можно использовать для замены тегов темы сетки событий.</span><span class="sxs-lookup"><span data-stu-id="7e978-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="7e978-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7e978-111">EXAMPLES</span></span>

### <span data-ttu-id="7e978-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7e978-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="7e978-113">Задает свойства темы "Сетка мероприятий" "Тема1" в группе ресурсов \` \` \` MyResourceGroupName, заменив теги указанными тегами \` "Отдел" и "Среда".</span><span class="sxs-lookup"><span data-stu-id="7e978-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="7e978-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e978-114">PARAMETERS</span></span>

### <span data-ttu-id="7e978-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e978-115">-DefaultProfile</span></span>
<span data-ttu-id="7e978-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7e978-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e978-117">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="7e978-117">-InboundIpRule</span></span>
<span data-ttu-id="7e978-118">Hashtable, представляющие список правил для входящие IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="7e978-118">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="7e978-119">Для каждого правила указывается IP-адрес в нотации CIDR, например 10.0.0.0.8, а также соответствующее действие, выполняемого на основе совпадения или отсутствие совпадений IpMask.</span><span class="sxs-lookup"><span data-stu-id="7e978-119">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="7e978-120">Возможные значения действий: "Только разрешить"</span><span class="sxs-lookup"><span data-stu-id="7e978-120">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e978-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e978-121">-InputObject</span></span>
<span data-ttu-id="7e978-122">Объект EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="7e978-122">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e978-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7e978-123">-Name</span></span>
<span data-ttu-id="7e978-124">Имя темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="7e978-124">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e978-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="7e978-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="7e978-126">Это определяет, разрешен ли трафик по общедоступным сетям.</span><span class="sxs-lookup"><span data-stu-id="7e978-126">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="7e978-127">По умолчанию она включена.</span><span class="sxs-lookup"><span data-stu-id="7e978-127">By default it is enabled.</span></span> <span data-ttu-id="7e978-128">Настраивая параметры InboundIpRule, вы можете ограничить их определенными параметрами.</span><span class="sxs-lookup"><span data-stu-id="7e978-128">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="7e978-129">Разрешенные значения отключены и включены.</span><span class="sxs-lookup"><span data-stu-id="7e978-129">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:
Accepted values: enabled, disabled

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases:
Accepted values: enabled, disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e978-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e978-130">-ResourceGroupName</span></span>
<span data-ttu-id="7e978-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e978-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e978-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e978-132">-ResourceId</span></span>
<span data-ttu-id="7e978-133">EventGrid Topic ResourceID.</span><span class="sxs-lookup"><span data-stu-id="7e978-133">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e978-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="7e978-134">-Tag</span></span>
<span data-ttu-id="7e978-135">Hashtables which represents resource Tag.</span><span class="sxs-lookup"><span data-stu-id="7e978-135">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e978-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e978-136">-Confirm</span></span>
<span data-ttu-id="7e978-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7e978-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e978-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e978-138">-WhatIf</span></span>
<span data-ttu-id="7e978-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e978-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e978-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7e978-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e978-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e978-141">CommonParameters</span></span>
<span data-ttu-id="7e978-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e978-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e978-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e978-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e978-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e978-144">INPUTS</span></span>

### <span data-ttu-id="7e978-145">System.String</span><span class="sxs-lookup"><span data-stu-id="7e978-145">System.String</span></span>

### <span data-ttu-id="7e978-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="7e978-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="7e978-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7e978-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7e978-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7e978-148">OUTPUTS</span></span>

### <span data-ttu-id="7e978-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="7e978-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="7e978-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7e978-150">NOTES</span></span>

## <span data-ttu-id="7e978-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e978-151">RELATED LINKS</span></span>
