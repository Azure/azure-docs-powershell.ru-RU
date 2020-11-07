---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 4717775f840d816b8f99cc64c4036d5563e8d849
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905401"
---
# <span data-ttu-id="2b799-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2b799-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="2b799-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b799-102">SYNOPSIS</span></span>
<span data-ttu-id="2b799-103">Возвращает описание указанного правила авторизации для заданного пространства имен, очереди или темы или псевдонима (конфигурации GeoDR).</span><span class="sxs-lookup"><span data-stu-id="2b799-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="2b799-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b799-104">SYNTAX</span></span>

### <span data-ttu-id="2b799-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2b799-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b799-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b799-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b799-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b799-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b799-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b799-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b799-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b799-109">DESCRIPTION</span></span>
<span data-ttu-id="2b799-110">Командлет **Get-AzServiceBusAuthorizationRule** получает описание указанного правила авторизации в заданном пространстве имен или в очереди или разделе или псевдониме (конфигурации GeoDR).</span><span class="sxs-lookup"><span data-stu-id="2b799-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="2b799-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b799-111">EXAMPLES</span></span>

### <span data-ttu-id="2b799-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2b799-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="2b799-113">Возвращает указанное описание правила авторизации для указанного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="2b799-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="2b799-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2b799-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="2b799-115">Возвращает указанное описание правила авторизации для указанной очереди.</span><span class="sxs-lookup"><span data-stu-id="2b799-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="2b799-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2b799-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="2b799-117">Возвращает указанное описание правила авторизации для указанной темы.</span><span class="sxs-lookup"><span data-stu-id="2b799-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="2b799-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="2b799-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="2b799-119">Возвращает указанное описание правила авторизации для указанного пространства имен и псевдонима.</span><span class="sxs-lookup"><span data-stu-id="2b799-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="2b799-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b799-120">PARAMETERS</span></span>

### <span data-ttu-id="2b799-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="2b799-121">-AliasName</span></span>
<span data-ttu-id="2b799-122">Имя конфигурации GeoDR</span><span class="sxs-lookup"><span data-stu-id="2b799-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="2b799-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b799-123">-DefaultProfile</span></span>
<span data-ttu-id="2b799-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b799-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b799-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2b799-125">-Name</span></span>
<span data-ttu-id="2b799-126">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2b799-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="2b799-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2b799-127">-Namespace</span></span>
<span data-ttu-id="2b799-128">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="2b799-128">Namespace Name</span></span>

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

### <span data-ttu-id="2b799-129">-Очередь</span><span class="sxs-lookup"><span data-stu-id="2b799-129">-Queue</span></span>
<span data-ttu-id="2b799-130">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="2b799-130">Queue Name</span></span>

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

### <span data-ttu-id="2b799-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b799-131">-ResourceGroupName</span></span>
<span data-ttu-id="2b799-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2b799-132">Resource Group Name</span></span>

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

### <span data-ttu-id="2b799-133">-Темы</span><span class="sxs-lookup"><span data-stu-id="2b799-133">-Topic</span></span>
<span data-ttu-id="2b799-134">Название раздела</span><span class="sxs-lookup"><span data-stu-id="2b799-134">Topic Name</span></span>

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

### <span data-ttu-id="2b799-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b799-135">CommonParameters</span></span>
<span data-ttu-id="2b799-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b799-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b799-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b799-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b799-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b799-138">INPUTS</span></span>

### <span data-ttu-id="2b799-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2b799-139">System.String</span></span>

## <span data-ttu-id="2b799-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b799-140">OUTPUTS</span></span>

### <span data-ttu-id="2b799-141">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="2b799-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="2b799-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b799-142">NOTES</span></span>

## <span data-ttu-id="2b799-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b799-143">RELATED LINKS</span></span>
