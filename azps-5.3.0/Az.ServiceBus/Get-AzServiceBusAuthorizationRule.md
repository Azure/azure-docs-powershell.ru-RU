---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e0f6c8c2b07c0d9ab788504bb8eae3eb4615a7e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517490"
---
# <span data-ttu-id="267b4-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="267b4-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="267b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="267b4-102">SYNOPSIS</span></span>
<span data-ttu-id="267b4-103">Описание указанного правила авторизации для определенного пространства имен, очереди или раздела или псевдонима (GeoDR Configurations).</span><span class="sxs-lookup"><span data-stu-id="267b4-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="267b4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="267b4-104">SYNTAX</span></span>

### <span data-ttu-id="267b4-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="267b4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="267b4-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="267b4-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="267b4-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="267b4-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="267b4-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="267b4-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="267b4-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="267b4-109">DESCRIPTION</span></span>
<span data-ttu-id="267b4-110">Для получения описания указанного правила авторизации в заданном пространстве имен, очереди, теме или псевдониме (GeoDR Configurations) можно получить описание указанного правила **авторизации.**</span><span class="sxs-lookup"><span data-stu-id="267b4-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="267b4-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="267b4-111">EXAMPLES</span></span>

### <span data-ttu-id="267b4-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="267b4-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="267b4-113">Возвращает описание указанного правила авторизации для указанного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="267b4-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="267b4-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="267b4-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="267b4-115">Возвращает описание заданного правила авторизации для указанной очереди.</span><span class="sxs-lookup"><span data-stu-id="267b4-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="267b4-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="267b4-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="267b4-117">Возвращает описание указанного правила авторизации для указанного раздела.</span><span class="sxs-lookup"><span data-stu-id="267b4-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="267b4-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="267b4-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="267b4-119">Возвращает описание указанного правила авторизации для указанного пространства имен и псевдонима.</span><span class="sxs-lookup"><span data-stu-id="267b4-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="267b4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="267b4-120">PARAMETERS</span></span>

### <span data-ttu-id="267b4-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="267b4-121">-AliasName</span></span>
<span data-ttu-id="267b4-122">Имя конфигурации GeoDR</span><span class="sxs-lookup"><span data-stu-id="267b4-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="267b4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="267b4-123">-DefaultProfile</span></span>
<span data-ttu-id="267b4-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="267b4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="267b4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="267b4-125">-Name</span></span>
<span data-ttu-id="267b4-126">Имяrule authorizationRule</span><span class="sxs-lookup"><span data-stu-id="267b4-126">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="267b4-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="267b4-127">-Namespace</span></span>
<span data-ttu-id="267b4-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="267b4-128">Namespace Name</span></span>

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

### <span data-ttu-id="267b4-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="267b4-129">-Queue</span></span>
<span data-ttu-id="267b4-130">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="267b4-130">Queue Name</span></span>

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

### <span data-ttu-id="267b4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="267b4-131">-ResourceGroupName</span></span>
<span data-ttu-id="267b4-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="267b4-132">Resource Group Name</span></span>

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

### <span data-ttu-id="267b4-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="267b4-133">-Topic</span></span>
<span data-ttu-id="267b4-134">Название темы</span><span class="sxs-lookup"><span data-stu-id="267b4-134">Topic Name</span></span>

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

### <span data-ttu-id="267b4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="267b4-135">CommonParameters</span></span>
<span data-ttu-id="267b4-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="267b4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="267b4-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="267b4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="267b4-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="267b4-138">INPUTS</span></span>

### <span data-ttu-id="267b4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="267b4-139">System.String</span></span>

## <span data-ttu-id="267b4-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="267b4-140">OUTPUTS</span></span>

### <span data-ttu-id="267b4-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="267b4-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="267b4-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="267b4-142">NOTES</span></span>

## <span data-ttu-id="267b4-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="267b4-143">RELATED LINKS</span></span>
