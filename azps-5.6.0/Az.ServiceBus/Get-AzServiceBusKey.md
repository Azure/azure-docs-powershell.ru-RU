---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: 28ecd68167a7db2f41ee64a38a4616548707096c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979267"
---
# <span data-ttu-id="7dcbc-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="7dcbc-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="7dcbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dcbc-102">SYNOPSIS</span></span>
<span data-ttu-id="7dcbc-103">Возвращает строки основного и дополнительного подключения для заданного пространства имен, очереди или раздела или псевдонима (GeoDR Configurations).</span><span class="sxs-lookup"><span data-stu-id="7dcbc-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="7dcbc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7dcbc-104">SYNTAX</span></span>

### <span data-ttu-id="7dcbc-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7dcbc-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7dcbc-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7dcbc-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7dcbc-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7dcbc-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7dcbc-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="7dcbc-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dcbc-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7dcbc-109">DESCRIPTION</span></span>
<span data-ttu-id="7dcbc-110">Cmdlet **Get-AzServiceBusKey** возвращает строки основного и дополнительного подключения для заданного пространства имен, очереди или раздела или псевдонима (GeoDR Configurations).</span><span class="sxs-lookup"><span data-stu-id="7dcbc-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="7dcbc-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7dcbc-111">EXAMPLES</span></span>

### <span data-ttu-id="7dcbc-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7dcbc-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="7dcbc-113">Строка основного и дополнительного соединения с указанным пространством имен.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="7dcbc-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7dcbc-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="7dcbc-115">Строка основного и дополнительного подключения к указанной очереди.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="7dcbc-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7dcbc-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="7dcbc-117">Строка основного и дополнительного подключения к указанному разделу.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="7dcbc-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="7dcbc-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="7dcbc-119">Строка основного и дополнительного подключения к указанному пространству имен и псевдониму.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="7dcbc-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7dcbc-120">PARAMETERS</span></span>

### <span data-ttu-id="7dcbc-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="7dcbc-121">-AliasName</span></span>
<span data-ttu-id="7dcbc-122">Имя псевдонима</span><span class="sxs-lookup"><span data-stu-id="7dcbc-122">Alias Name</span></span>

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

### <span data-ttu-id="7dcbc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dcbc-123">-DefaultProfile</span></span>
<span data-ttu-id="7dcbc-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dcbc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7dcbc-125">-Name</span></span>
<span data-ttu-id="7dcbc-126">Имяrule authorizationRule</span><span class="sxs-lookup"><span data-stu-id="7dcbc-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="7dcbc-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7dcbc-127">-Namespace</span></span>
<span data-ttu-id="7dcbc-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="7dcbc-128">Namespace Name</span></span>

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

### <span data-ttu-id="7dcbc-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="7dcbc-129">-Queue</span></span>
<span data-ttu-id="7dcbc-130">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="7dcbc-130">Queue Name</span></span>

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

### <span data-ttu-id="7dcbc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dcbc-131">-ResourceGroupName</span></span>
<span data-ttu-id="7dcbc-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7dcbc-132">Resource Group Name</span></span>

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

### <span data-ttu-id="7dcbc-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="7dcbc-133">-Topic</span></span>
<span data-ttu-id="7dcbc-134">Название темы</span><span class="sxs-lookup"><span data-stu-id="7dcbc-134">Topic Name</span></span>

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

### <span data-ttu-id="7dcbc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dcbc-135">CommonParameters</span></span>
<span data-ttu-id="7dcbc-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dcbc-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dcbc-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dcbc-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7dcbc-138">INPUTS</span></span>

### <span data-ttu-id="7dcbc-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7dcbc-139">System.String</span></span>

## <span data-ttu-id="7dcbc-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7dcbc-140">OUTPUTS</span></span>

### <span data-ttu-id="7dcbc-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="7dcbc-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="7dcbc-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7dcbc-142">NOTES</span></span>

## <span data-ttu-id="7dcbc-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7dcbc-143">RELATED LINKS</span></span>
