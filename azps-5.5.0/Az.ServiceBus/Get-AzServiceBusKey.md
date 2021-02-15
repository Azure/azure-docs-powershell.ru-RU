---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: ffe220510f3046ea10b6374eb48c3c74730e4bc2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217601"
---
# <span data-ttu-id="c5779-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="c5779-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="c5779-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5779-102">SYNOPSIS</span></span>
<span data-ttu-id="c5779-103">Возвращает строки основного и дополнительного подключения для заданного пространства имен, очереди или раздела или псевдонима (GeoDR Configurations).</span><span class="sxs-lookup"><span data-stu-id="c5779-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="c5779-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c5779-104">SYNTAX</span></span>

### <span data-ttu-id="c5779-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c5779-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5779-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c5779-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5779-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c5779-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5779-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="c5779-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5779-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5779-109">DESCRIPTION</span></span>
<span data-ttu-id="c5779-110">Cmdlet **Get-AzServiceBusKey** возвращает строки основного и дополнительного подключения для заданного пространства имен, очереди или раздела или псевдонима (GeoDR Configurations).</span><span class="sxs-lookup"><span data-stu-id="c5779-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="c5779-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c5779-111">EXAMPLES</span></span>

### <span data-ttu-id="c5779-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c5779-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="c5779-113">Строка основного и дополнительного соединения с указанным пространством имен.</span><span class="sxs-lookup"><span data-stu-id="c5779-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="c5779-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c5779-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="c5779-115">Строка основного и дополнительного подключения к указанной очереди.</span><span class="sxs-lookup"><span data-stu-id="c5779-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="c5779-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c5779-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="c5779-117">Строка основного и дополнительного подключения к указанному разделу.</span><span class="sxs-lookup"><span data-stu-id="c5779-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="c5779-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="c5779-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="c5779-119">Строка основного и дополнительного подключения к указанному пространству имен и псевдониму.</span><span class="sxs-lookup"><span data-stu-id="c5779-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="c5779-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5779-120">PARAMETERS</span></span>

### <span data-ttu-id="c5779-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="c5779-121">-AliasName</span></span>
<span data-ttu-id="c5779-122">Имя псевдонима</span><span class="sxs-lookup"><span data-stu-id="c5779-122">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5779-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5779-123">-DefaultProfile</span></span>
<span data-ttu-id="c5779-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5779-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5779-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c5779-125">-Name</span></span>
<span data-ttu-id="c5779-126">Имяrule authorizationRule</span><span class="sxs-lookup"><span data-stu-id="c5779-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="c5779-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c5779-127">-Namespace</span></span>
<span data-ttu-id="c5779-128">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="c5779-128">Namespace Name</span></span>

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

### <span data-ttu-id="c5779-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="c5779-129">-Queue</span></span>
<span data-ttu-id="c5779-130">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="c5779-130">Queue Name</span></span>

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

### <span data-ttu-id="c5779-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5779-131">-ResourceGroupName</span></span>
<span data-ttu-id="c5779-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c5779-132">Resource Group Name</span></span>

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

### <span data-ttu-id="c5779-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="c5779-133">-Topic</span></span>
<span data-ttu-id="c5779-134">Название темы</span><span class="sxs-lookup"><span data-stu-id="c5779-134">Topic Name</span></span>

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

### <span data-ttu-id="c5779-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5779-135">CommonParameters</span></span>
<span data-ttu-id="c5779-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5779-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5779-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5779-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5779-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5779-138">INPUTS</span></span>

### <span data-ttu-id="c5779-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c5779-139">System.String</span></span>

## <span data-ttu-id="c5779-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c5779-140">OUTPUTS</span></span>

### <span data-ttu-id="c5779-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="c5779-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="c5779-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c5779-142">NOTES</span></span>

## <span data-ttu-id="c5779-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5779-143">RELATED LINKS</span></span>
