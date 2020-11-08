---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: ffe220510f3046ea10b6374eb48c3c74730e4bc2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077629"
---
# <span data-ttu-id="f80e7-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="f80e7-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="f80e7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f80e7-102">SYNOPSIS</span></span>
<span data-ttu-id="f80e7-103">Получает первичные и дополнительные строки подключения для заданного пространства имен, очереди или темы или псевдонима (конфигурации GeoDR).</span><span class="sxs-lookup"><span data-stu-id="f80e7-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="f80e7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f80e7-104">SYNTAX</span></span>

### <span data-ttu-id="f80e7-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f80e7-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f80e7-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f80e7-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f80e7-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f80e7-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f80e7-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="f80e7-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f80e7-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f80e7-109">DESCRIPTION</span></span>
<span data-ttu-id="f80e7-110">Командлет **Get-AzServiceBusKey** возвращает первичные и дополнительные строки подключения для данного пространства имен, очереди или темы или псевдонима (конфигурации GeoDR).</span><span class="sxs-lookup"><span data-stu-id="f80e7-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="f80e7-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f80e7-111">EXAMPLES</span></span>

### <span data-ttu-id="f80e7-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f80e7-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="f80e7-113">Основной и дополнительный строки подключения к указанному пространству имен.</span><span class="sxs-lookup"><span data-stu-id="f80e7-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="f80e7-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f80e7-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="f80e7-115">Основной и дополнительный строки подключения к указанной очереди.</span><span class="sxs-lookup"><span data-stu-id="f80e7-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="f80e7-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f80e7-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="f80e7-117">Основной и дополнительный строки соединения с указанным разделом.</span><span class="sxs-lookup"><span data-stu-id="f80e7-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="f80e7-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="f80e7-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="f80e7-119">Основной и дополнительный строки соединения с указанным пространством имен и псевдонимом.</span><span class="sxs-lookup"><span data-stu-id="f80e7-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="f80e7-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f80e7-120">PARAMETERS</span></span>

### <span data-ttu-id="f80e7-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="f80e7-121">-AliasName</span></span>
<span data-ttu-id="f80e7-122">Имя псевдонима</span><span class="sxs-lookup"><span data-stu-id="f80e7-122">Alias Name</span></span>

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

### <span data-ttu-id="f80e7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f80e7-123">-DefaultProfile</span></span>
<span data-ttu-id="f80e7-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f80e7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f80e7-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f80e7-125">-Name</span></span>
<span data-ttu-id="f80e7-126">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f80e7-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="f80e7-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f80e7-127">-Namespace</span></span>
<span data-ttu-id="f80e7-128">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="f80e7-128">Namespace Name</span></span>

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

### <span data-ttu-id="f80e7-129">-Очередь</span><span class="sxs-lookup"><span data-stu-id="f80e7-129">-Queue</span></span>
<span data-ttu-id="f80e7-130">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="f80e7-130">Queue Name</span></span>

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

### <span data-ttu-id="f80e7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f80e7-131">-ResourceGroupName</span></span>
<span data-ttu-id="f80e7-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f80e7-132">Resource Group Name</span></span>

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

### <span data-ttu-id="f80e7-133">-Темы</span><span class="sxs-lookup"><span data-stu-id="f80e7-133">-Topic</span></span>
<span data-ttu-id="f80e7-134">Название раздела</span><span class="sxs-lookup"><span data-stu-id="f80e7-134">Topic Name</span></span>

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

### <span data-ttu-id="f80e7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f80e7-135">CommonParameters</span></span>
<span data-ttu-id="f80e7-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f80e7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f80e7-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f80e7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f80e7-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f80e7-138">INPUTS</span></span>

### <span data-ttu-id="f80e7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f80e7-139">System.String</span></span>

## <span data-ttu-id="f80e7-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f80e7-140">OUTPUTS</span></span>

### <span data-ttu-id="f80e7-141">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="f80e7-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="f80e7-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="f80e7-142">NOTES</span></span>

## <span data-ttu-id="f80e7-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f80e7-143">RELATED LINKS</span></span>
