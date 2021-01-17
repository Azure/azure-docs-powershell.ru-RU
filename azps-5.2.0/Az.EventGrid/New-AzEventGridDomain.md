---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 6340db7446671660df08449529b6678cf79a2af9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329535"
---
# <span data-ttu-id="6c4ab-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6c4ab-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="6c4ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c4ab-102">SYNOPSIS</span></span>
<span data-ttu-id="6c4ab-103">Создание домена Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="6c4ab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6c4ab-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c4ab-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c4ab-105">DESCRIPTION</span></span>
<span data-ttu-id="6c4ab-106">Создание домена Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="6c4ab-107">После создания домена приложение может публиковать события на конечной точке темы.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="6c4ab-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6c4ab-108">EXAMPLES</span></span>

### <span data-ttu-id="6c4ab-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6c4ab-109">Example 1</span></span>

<span data-ttu-id="6c4ab-110">Создание домена Event Grid Domain1 в указанном географическом расположении westus2 в группе ресурсов \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="6c4ab-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="6c4ab-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6c4ab-111">Example 2</span></span>

<span data-ttu-id="6c4ab-112">Создание домена Event Grid Domain1 в указанном географическом расположении westus2 в группе ресурсов \` MyResourceGroupName с указанными тегами \` \` \` \` \` "Department" и "Environment".</span><span class="sxs-lookup"><span data-stu-id="6c4ab-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Department, Finance], [Environment, Test]}
```

## <span data-ttu-id="6c4ab-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c4ab-113">PARAMETERS</span></span>

### <span data-ttu-id="6c4ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c4ab-114">-DefaultProfile</span></span>
<span data-ttu-id="6c4ab-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c4ab-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="6c4ab-116">-InboundIpRule</span></span>
<span data-ttu-id="6c4ab-117">Hashtable, представляющие список правил для входящие IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="6c4ab-118">Для каждого правила указывается IP-адрес в нотации CIDR, например 10.0.0.0.8, а также соответствующее действие, выполняемого на основе совпадения или отсутствие совпадений IpMask.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="6c4ab-119">Возможные значения действий: "Только разрешить"</span><span class="sxs-lookup"><span data-stu-id="6c4ab-119">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4ab-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="6c4ab-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="6c4ab-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="6c4ab-122">Допустимые имена ключей: subject, eventtype и dataversion.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="6c4ab-123">Это используется, если InputSchemaHelp является только настраиваемойventschema.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4ab-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="6c4ab-124">-InputMappingField</span></span>
<span data-ttu-id="6c4ab-125">Hashtable which represents the input mapping fields in space separated key = value format.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="6c4ab-126">Допустимые имена ключей: id, topic, eventtime, subject, eventtype и dataversion.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="6c4ab-127">Это используется, если InputSchemaHelp является только настраиваемойventschema.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4ab-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="6c4ab-128">-InputSchema</span></span>
<span data-ttu-id="6c4ab-129">Схема входных событий для темы.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="6c4ab-130">Допустимые значения: eventgridschema, customeventschema или cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="6c4ab-131">Значение по умолчанию — eventgridschema.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-131">Default value is eventgridschema.</span></span> <span data-ttu-id="6c4ab-132">Обратите внимание, что если задан параметр customeventschema, параметры InputMappingField или/и InputMappingDefaultValue также должны быть указаны.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EventGridSchema, CustomEventSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4ab-133">-Location</span><span class="sxs-lookup"><span data-stu-id="6c4ab-133">-Location</span></span>
<span data-ttu-id="6c4ab-134">Расположение домена.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-134">The location of the domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4ab-135">-Name</span><span class="sxs-lookup"><span data-stu-id="6c4ab-135">-Name</span></span>
<span data-ttu-id="6c4ab-136">Доменное имя EventGrid.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-136">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4ab-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="6c4ab-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="6c4ab-138">Это определяет, разрешен ли трафик по общедоступным сетям.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="6c4ab-139">По умолчанию она включена.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-139">By default it is enabled.</span></span> <span data-ttu-id="6c4ab-140">Настраивая параметры InboundIpRule, вы можете ограничить их определенными параметрами.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="6c4ab-141">Разрешенные значения отключены и включены.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-141">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4ab-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c4ab-142">-ResourceGroupName</span></span>
<span data-ttu-id="6c4ab-143">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4ab-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="6c4ab-144">-Tag</span></span>
<span data-ttu-id="6c4ab-145">Hashtable which represents resource Tags.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-145">Hashtable which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4ab-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c4ab-146">-Confirm</span></span>
<span data-ttu-id="6c4ab-147">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c4ab-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c4ab-148">-WhatIf</span></span>
<span data-ttu-id="6c4ab-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c4ab-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c4ab-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c4ab-151">CommonParameters</span></span>
<span data-ttu-id="6c4ab-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c4ab-153">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c4ab-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c4ab-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c4ab-154">INPUTS</span></span>

### <span data-ttu-id="6c4ab-155">System.String</span><span class="sxs-lookup"><span data-stu-id="6c4ab-155">System.String</span></span>

### <span data-ttu-id="6c4ab-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6c4ab-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6c4ab-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6c4ab-157">OUTPUTS</span></span>

### <span data-ttu-id="6c4ab-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="6c4ab-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="6c4ab-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6c4ab-159">NOTES</span></span>

## <span data-ttu-id="6c4ab-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c4ab-160">RELATED LINKS</span></span>
