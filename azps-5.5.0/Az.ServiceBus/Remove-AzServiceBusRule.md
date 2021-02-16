---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: a3fc0d37e48ddeba41b6870edfe1732eeecfaa14
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235692"
---
# <span data-ttu-id="4ea38-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="4ea38-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="4ea38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ea38-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea38-103">Удаляет указанное правило для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="4ea38-103">Removes the specified rule of a given subscription .</span></span>

## <span data-ttu-id="4ea38-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4ea38-104">SYNTAX</span></span>

### <span data-ttu-id="4ea38-105">Набор свойств правил (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ea38-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ea38-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4ea38-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ea38-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ea38-107">DESCRIPTION</span></span>
<span data-ttu-id="4ea38-108">С **его учетом** удаляется правило подписки на данную тему.</span><span class="sxs-lookup"><span data-stu-id="4ea38-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="4ea38-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4ea38-109">EXAMPLES</span></span>

### <span data-ttu-id="4ea38-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4ea38-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="4ea38-111">Удаляет правило `SBRule` подписки `SBSubscription` для указанного `SBTopic` раздела.</span><span class="sxs-lookup"><span data-stu-id="4ea38-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="4ea38-112">Пример 2. InputObject — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="4ea38-112">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="4ea38-113">Удаляет правило, предоставленное $inputobject параметра -InputObject.</span><span class="sxs-lookup"><span data-stu-id="4ea38-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="4ea38-114">Пример 3. InputObject — использование piping:</span><span class="sxs-lookup"><span data-stu-id="4ea38-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="4ea38-115">Пример 4. ResourceId — использование переменной</span><span class="sxs-lookup"><span data-stu-id="4ea38-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="4ea38-116">Пример 5. ResourceId — использование строки</span><span class="sxs-lookup"><span data-stu-id="4ea38-116">Example 5: ResourceId - Using string value</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="4ea38-117">Удаляет правило, предоставленное с помощью ARM в параметре $resourceid-ResourceId/string для параметра -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="4ea38-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="4ea38-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ea38-118">PARAMETERS</span></span>

### <span data-ttu-id="4ea38-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ea38-119">-AsJob</span></span>
<span data-ttu-id="4ea38-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4ea38-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ea38-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea38-121">-DefaultProfile</span></span>
<span data-ttu-id="4ea38-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea38-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ea38-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4ea38-123">-Force</span></span>
<span data-ttu-id="4ea38-124">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="4ea38-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4ea38-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ea38-125">-InputObject</span></span>
<span data-ttu-id="4ea38-126">Объект "Правило обслуживания"</span><span class="sxs-lookup"><span data-stu-id="4ea38-126">Service Bus Rule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea38-127">-Name</span><span class="sxs-lookup"><span data-stu-id="4ea38-127">-Name</span></span>
<span data-ttu-id="4ea38-128">Имя правила</span><span class="sxs-lookup"><span data-stu-id="4ea38-128">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea38-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4ea38-129">-Namespace</span></span>
<span data-ttu-id="4ea38-130">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="4ea38-130">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea38-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ea38-131">-PassThru</span></span>
<span data-ttu-id="4ea38-132">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="4ea38-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4ea38-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ea38-133">-ResourceGroupName</span></span>
<span data-ttu-id="4ea38-134">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4ea38-134">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea38-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ea38-135">-ResourceId</span></span>
<span data-ttu-id="4ea38-136">Service Bus Rule Resource Id</span><span class="sxs-lookup"><span data-stu-id="4ea38-136">Service Bus Rule Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea38-137">-Подписка</span><span class="sxs-lookup"><span data-stu-id="4ea38-137">-Subscription</span></span>
<span data-ttu-id="4ea38-138">Имя подписки</span><span class="sxs-lookup"><span data-stu-id="4ea38-138">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea38-139">-Topic</span><span class="sxs-lookup"><span data-stu-id="4ea38-139">-Topic</span></span>
<span data-ttu-id="4ea38-140">Название темы</span><span class="sxs-lookup"><span data-stu-id="4ea38-140">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea38-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ea38-141">-Confirm</span></span>
<span data-ttu-id="4ea38-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ea38-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ea38-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ea38-143">-WhatIf</span></span>
<span data-ttu-id="4ea38-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ea38-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ea38-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4ea38-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ea38-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea38-146">CommonParameters</span></span>
<span data-ttu-id="4ea38-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ea38-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea38-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ea38-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea38-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ea38-149">INPUTS</span></span>

### <span data-ttu-id="4ea38-150">System.String</span><span class="sxs-lookup"><span data-stu-id="4ea38-150">System.String</span></span>

### <span data-ttu-id="4ea38-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="4ea38-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="4ea38-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4ea38-152">OUTPUTS</span></span>

### <span data-ttu-id="4ea38-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4ea38-153">System.Boolean</span></span>

## <span data-ttu-id="4ea38-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4ea38-154">NOTES</span></span>

## <span data-ttu-id="4ea38-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ea38-155">RELATED LINKS</span></span>
