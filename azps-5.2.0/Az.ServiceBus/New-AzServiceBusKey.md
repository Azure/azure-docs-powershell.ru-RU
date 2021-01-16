---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: c0c413918a986da4eaea8d9ef5f0f6a091b8b2e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412028"
---
# <span data-ttu-id="69b55-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="69b55-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="69b55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69b55-102">SYNOPSIS</span></span>
<span data-ttu-id="69b55-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span><span class="sxs-lookup"><span data-stu-id="69b55-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="69b55-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="69b55-104">SYNTAX</span></span>

### <span data-ttu-id="69b55-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="69b55-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69b55-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="69b55-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69b55-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="69b55-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69b55-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69b55-108">DESCRIPTION</span></span>
<span data-ttu-id="69b55-109">Для указанного пространства имен, очереди или темы и правила авторизации с его нажатием создается новая строка основного или дополнительного подключения **New-AzServiceBusKey.**</span><span class="sxs-lookup"><span data-stu-id="69b55-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="69b55-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="69b55-110">EXAMPLES</span></span>

### <span data-ttu-id="69b55-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="69b55-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="69b55-112">Regenerates the primary or secondary connection strings for the namespace.</span><span class="sxs-lookup"><span data-stu-id="69b55-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="69b55-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="69b55-113">Example 2</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="69b55-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span><span class="sxs-lookup"><span data-stu-id="69b55-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="69b55-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="69b55-115">Example 3</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="69b55-116">Повторное сгенерирует строки основного или дополнительного подключения для очереди.</span><span class="sxs-lookup"><span data-stu-id="69b55-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="69b55-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="69b55-117">Example 4</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="69b55-118">Повторное сгенерирует строки основного или дополнительного подключения с задамым значением ключа для очереди.</span><span class="sxs-lookup"><span data-stu-id="69b55-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="69b55-119">Пример 5</span><span class="sxs-lookup"><span data-stu-id="69b55-119">Example 5</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="69b55-120">Повторное сгенерирует строки основного или дополнительного подключения для этого раздела.</span><span class="sxs-lookup"><span data-stu-id="69b55-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="69b55-121">Пример 6</span><span class="sxs-lookup"><span data-stu-id="69b55-121">Example 6</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="69b55-122">Повторное сгенерирует строки основного или дополнительного подключения с заданной ключевой строкой для данной темы.</span><span class="sxs-lookup"><span data-stu-id="69b55-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="69b55-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69b55-123">PARAMETERS</span></span>

### <span data-ttu-id="69b55-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69b55-124">-DefaultProfile</span></span>
<span data-ttu-id="69b55-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69b55-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69b55-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="69b55-126">-KeyValue</span></span>
<span data-ttu-id="69b55-127">Ключ 256-битной кодировки base64 для подписания и проверки маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="69b55-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="69b55-128">-Name</span><span class="sxs-lookup"><span data-stu-id="69b55-128">-Name</span></span>
<span data-ttu-id="69b55-129">Имяrule authorizationRule.</span><span class="sxs-lookup"><span data-stu-id="69b55-129">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69b55-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="69b55-130">-Namespace</span></span>
<span data-ttu-id="69b55-131">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="69b55-131">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69b55-132">-Queue</span><span class="sxs-lookup"><span data-stu-id="69b55-132">-Queue</span></span>
<span data-ttu-id="69b55-133">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="69b55-133">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69b55-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="69b55-134">-RegenerateKey</span></span>
<span data-ttu-id="69b55-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span><span class="sxs-lookup"><span data-stu-id="69b55-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69b55-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69b55-136">-ResourceGroupName</span></span>
<span data-ttu-id="69b55-137">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="69b55-137">Resource Group Name</span></span>

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

### <span data-ttu-id="69b55-138">-Topic</span><span class="sxs-lookup"><span data-stu-id="69b55-138">-Topic</span></span>
<span data-ttu-id="69b55-139">Название темы</span><span class="sxs-lookup"><span data-stu-id="69b55-139">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69b55-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69b55-140">-Confirm</span></span>
<span data-ttu-id="69b55-141">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="69b55-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69b55-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69b55-142">-WhatIf</span></span>
<span data-ttu-id="69b55-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69b55-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69b55-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="69b55-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69b55-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69b55-145">CommonParameters</span></span>
<span data-ttu-id="69b55-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69b55-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69b55-147">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69b55-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69b55-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69b55-148">INPUTS</span></span>

### <span data-ttu-id="69b55-149">System.String</span><span class="sxs-lookup"><span data-stu-id="69b55-149">System.String</span></span>

## <span data-ttu-id="69b55-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="69b55-150">OUTPUTS</span></span>

### <span data-ttu-id="69b55-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="69b55-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="69b55-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="69b55-152">NOTES</span></span>

## <span data-ttu-id="69b55-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69b55-153">RELATED LINKS</span></span>
