---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e0f6c8c2b07c0d9ab788504bb8eae3eb4615a7e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245687"
---
# <span data-ttu-id="1fb2e-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1fb2e-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="1fb2e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1fb2e-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb2e-103">Возвращает описание указанного правила авторизации для заданного пространства имен, очереди или темы или псевдонима (конфигурации GeoDR).</span><span class="sxs-lookup"><span data-stu-id="1fb2e-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="1fb2e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1fb2e-104">SYNTAX</span></span>

### <span data-ttu-id="1fb2e-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1fb2e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fb2e-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1fb2e-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fb2e-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1fb2e-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fb2e-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="1fb2e-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fb2e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fb2e-109">DESCRIPTION</span></span>
<span data-ttu-id="1fb2e-110">Командлет **Get-AzServiceBusAuthorizationRule** получает описание указанного правила авторизации в заданном пространстве имен или в очереди или разделе или псевдониме (конфигурации GeoDR).</span><span class="sxs-lookup"><span data-stu-id="1fb2e-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="1fb2e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1fb2e-111">EXAMPLES</span></span>

### <span data-ttu-id="1fb2e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1fb2e-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="1fb2e-113">Возвращает указанное описание правила авторизации для указанного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1fb2e-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="1fb2e-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1fb2e-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="1fb2e-115">Возвращает указанное описание правила авторизации для указанной очереди.</span><span class="sxs-lookup"><span data-stu-id="1fb2e-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="1fb2e-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="1fb2e-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="1fb2e-117">Возвращает указанное описание правила авторизации для указанной темы.</span><span class="sxs-lookup"><span data-stu-id="1fb2e-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="1fb2e-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="1fb2e-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="1fb2e-119">Возвращает указанное описание правила авторизации для указанного пространства имен и псевдонима.</span><span class="sxs-lookup"><span data-stu-id="1fb2e-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="1fb2e-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1fb2e-120">PARAMETERS</span></span>

### <span data-ttu-id="1fb2e-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="1fb2e-121">-AliasName</span></span>
<span data-ttu-id="1fb2e-122">Имя конфигурации GeoDR</span><span class="sxs-lookup"><span data-stu-id="1fb2e-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="1fb2e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb2e-123">-DefaultProfile</span></span>
<span data-ttu-id="1fb2e-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb2e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fb2e-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1fb2e-125">-Name</span></span>
<span data-ttu-id="1fb2e-126">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1fb2e-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="1fb2e-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1fb2e-127">-Namespace</span></span>
<span data-ttu-id="1fb2e-128">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="1fb2e-128">Namespace Name</span></span>

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

### <span data-ttu-id="1fb2e-129">-Очередь</span><span class="sxs-lookup"><span data-stu-id="1fb2e-129">-Queue</span></span>
<span data-ttu-id="1fb2e-130">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="1fb2e-130">Queue Name</span></span>

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

### <span data-ttu-id="1fb2e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fb2e-131">-ResourceGroupName</span></span>
<span data-ttu-id="1fb2e-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1fb2e-132">Resource Group Name</span></span>

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

### <span data-ttu-id="1fb2e-133">-Темы</span><span class="sxs-lookup"><span data-stu-id="1fb2e-133">-Topic</span></span>
<span data-ttu-id="1fb2e-134">Название раздела</span><span class="sxs-lookup"><span data-stu-id="1fb2e-134">Topic Name</span></span>

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

### <span data-ttu-id="1fb2e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb2e-135">CommonParameters</span></span>
<span data-ttu-id="1fb2e-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1fb2e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb2e-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fb2e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb2e-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1fb2e-138">INPUTS</span></span>

### <span data-ttu-id="1fb2e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1fb2e-139">System.String</span></span>

## <span data-ttu-id="1fb2e-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fb2e-140">OUTPUTS</span></span>

### <span data-ttu-id="1fb2e-141">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="1fb2e-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="1fb2e-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="1fb2e-142">NOTES</span></span>

## <span data-ttu-id="1fb2e-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fb2e-143">RELATED LINKS</span></span>