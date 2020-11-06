---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: fa7224654581a5c71cb4daafa5dbb96100d63705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569195"
---
# <span data-ttu-id="ace7e-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ace7e-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="ace7e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ace7e-102">SYNOPSIS</span></span>
<span data-ttu-id="ace7e-103">Возвращает описание указанного правила авторизации для данного пространства имен или очереди или темы.</span><span class="sxs-lookup"><span data-stu-id="ace7e-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ace7e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ace7e-104">SYNTAX</span></span>

### <span data-ttu-id="ace7e-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ace7e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ace7e-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ace7e-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ace7e-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ace7e-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ace7e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ace7e-108">DESCRIPTION</span></span>
<span data-ttu-id="ace7e-109">Командлет **Get-AzureRmServiceBusAuthorizationRule** получает описание указанного правила авторизации в заданном пространстве имен или в очереди или разделе.</span><span class="sxs-lookup"><span data-stu-id="ace7e-109">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="ace7e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ace7e-110">EXAMPLES</span></span>

### <span data-ttu-id="ace7e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ace7e-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="ace7e-112">Возвращает указанное описание правила авторизации для указанного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="ace7e-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="ace7e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ace7e-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="ace7e-114">Возвращает указанное описание правила авторизации для указанной очереди.</span><span class="sxs-lookup"><span data-stu-id="ace7e-114">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="ace7e-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ace7e-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="ace7e-116">Возвращает указанное описание правила авторизации для указанной темы.</span><span class="sxs-lookup"><span data-stu-id="ace7e-116">Returns the specified authorization rule description for a specified topic.</span></span>

## <span data-ttu-id="ace7e-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ace7e-117">PARAMETERS</span></span>

### <span data-ttu-id="ace7e-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ace7e-118">-Name</span></span>
<span data-ttu-id="ace7e-119">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="ace7e-119">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="ace7e-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ace7e-120">-Namespace</span></span>
<span data-ttu-id="ace7e-121">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="ace7e-121">Namespace Name.</span></span>

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

### <span data-ttu-id="ace7e-122">-Очередь</span><span class="sxs-lookup"><span data-stu-id="ace7e-122">-Queue</span></span>
<span data-ttu-id="ace7e-123">Имя очереди.</span><span class="sxs-lookup"><span data-stu-id="ace7e-123">Queue Name.</span></span>

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

### <span data-ttu-id="ace7e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ace7e-124">-ResourceGroupName</span></span>
<span data-ttu-id="ace7e-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ace7e-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ace7e-126">-Темы</span><span class="sxs-lookup"><span data-stu-id="ace7e-126">-Topic</span></span>
<span data-ttu-id="ace7e-127">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="ace7e-127">Topic Name.</span></span>

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

### <span data-ttu-id="ace7e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ace7e-128">-DefaultProfile</span></span>
<span data-ttu-id="ace7e-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ace7e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ace7e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace7e-130">CommonParameters</span></span>
<span data-ttu-id="ace7e-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ace7e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace7e-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ace7e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace7e-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ace7e-133">INPUTS</span></span>

### <span data-ttu-id="ace7e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ace7e-134">System.String</span></span>

## <span data-ttu-id="ace7e-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ace7e-135">OUTPUTS</span></span>

### <span data-ttu-id="ace7e-136">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.4.2.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="ace7e-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ace7e-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ace7e-137">NOTES</span></span>
## <span data-ttu-id="ace7e-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ace7e-138">RELATED LINKS</span></span>

## <span data-ttu-id="ace7e-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ace7e-139">RELATED LINKS</span></span>

