---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: 28abf3ff725f5a1b124f99c96b46d03458b42f8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559532"
---
# <span data-ttu-id="69d56-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="69d56-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="69d56-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="69d56-102">SYNOPSIS</span></span>
<span data-ttu-id="69d56-103">Получает первичные и дополнительные строки подключения для заданного пространства имен или очереди или темы.</span><span class="sxs-lookup"><span data-stu-id="69d56-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69d56-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="69d56-104">SYNTAX</span></span>

### <span data-ttu-id="69d56-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="69d56-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69d56-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="69d56-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69d56-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="69d56-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69d56-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69d56-108">DESCRIPTION</span></span>
<span data-ttu-id="69d56-109">Командлет **Get-AzureRmServiceBusKey** возвращает первичные и дополнительные строки подключения для данного пространства имен или очереди или темы.</span><span class="sxs-lookup"><span data-stu-id="69d56-109">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span> 

## <span data-ttu-id="69d56-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="69d56-110">EXAMPLES</span></span>

### <span data-ttu-id="69d56-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="69d56-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="69d56-112">Основной и дополнительный строки подключения к указанному пространству имен.</span><span class="sxs-lookup"><span data-stu-id="69d56-112">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="69d56-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="69d56-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="69d56-114">Основной и дополнительный строки подключения к указанной очереди.</span><span class="sxs-lookup"><span data-stu-id="69d56-114">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="69d56-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="69d56-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="69d56-116">Основной и дополнительный строки соединения с указанным разделом.</span><span class="sxs-lookup"><span data-stu-id="69d56-116">Primary and secondary connection string to the specified topic.</span></span>

## <span data-ttu-id="69d56-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="69d56-117">PARAMETERS</span></span>

### <span data-ttu-id="69d56-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="69d56-118">-Name</span></span>
<span data-ttu-id="69d56-119">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="69d56-119">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="69d56-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="69d56-120">-Namespace</span></span>
<span data-ttu-id="69d56-121">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="69d56-121">Namespace Name.</span></span>

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

### <span data-ttu-id="69d56-122">-Очередь</span><span class="sxs-lookup"><span data-stu-id="69d56-122">-Queue</span></span>
<span data-ttu-id="69d56-123">Имя очереди.</span><span class="sxs-lookup"><span data-stu-id="69d56-123">Queue Name.</span></span>

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

### <span data-ttu-id="69d56-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69d56-124">-ResourceGroupName</span></span>
<span data-ttu-id="69d56-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="69d56-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="69d56-126">-Темы</span><span class="sxs-lookup"><span data-stu-id="69d56-126">-Topic</span></span>
<span data-ttu-id="69d56-127">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="69d56-127">Topic Name.</span></span>

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

### <span data-ttu-id="69d56-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69d56-128">-DefaultProfile</span></span>
<span data-ttu-id="69d56-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69d56-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69d56-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69d56-130">CommonParameters</span></span>
<span data-ttu-id="69d56-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="69d56-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69d56-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69d56-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69d56-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="69d56-133">INPUTS</span></span>

### <span data-ttu-id="69d56-134">System. String</span><span class="sxs-lookup"><span data-stu-id="69d56-134">System.String</span></span>

## <span data-ttu-id="69d56-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="69d56-135">OUTPUTS</span></span>

### <span data-ttu-id="69d56-136">Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="69d56-136">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="69d56-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="69d56-137">NOTES</span></span>

## <span data-ttu-id="69d56-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69d56-138">RELATED LINKS</span></span>

