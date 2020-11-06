---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: e5a4886eef132f0e48c146fa70889dfa283489b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561487"
---
# <span data-ttu-id="deb06-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="deb06-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="deb06-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="deb06-102">SYNOPSIS</span></span>
<span data-ttu-id="deb06-103">Возвращает описание указанного правила авторизации для заданного пространства имен, очереди или темы или псевдонима (конфигурации GeoDR).</span><span class="sxs-lookup"><span data-stu-id="deb06-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 


[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="deb06-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="deb06-104">SYNTAX</span></span>

### <span data-ttu-id="deb06-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="deb06-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="deb06-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="deb06-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="deb06-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="deb06-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="deb06-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="deb06-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-AliasName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="deb06-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="deb06-109">DESCRIPTION</span></span>
<span data-ttu-id="deb06-110">Командлет **Get-AzureRmServiceBusAuthorizationRule** получает описание указанного правила авторизации в заданном пространстве имен или в очереди или разделе или псевдониме (конфигурации GeoDR).</span><span class="sxs-lookup"><span data-stu-id="deb06-110">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="deb06-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="deb06-111">EXAMPLES</span></span>

### <span data-ttu-id="deb06-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="deb06-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="deb06-113">Возвращает указанное описание правила авторизации для указанного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="deb06-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="deb06-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="deb06-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="deb06-115">Возвращает указанное описание правила авторизации для указанной очереди.</span><span class="sxs-lookup"><span data-stu-id="deb06-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="deb06-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="deb06-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="deb06-117">Возвращает указанное описание правила авторизации для указанной темы.</span><span class="sxs-lookup"><span data-stu-id="deb06-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="deb06-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="deb06-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="deb06-119">Возвращает указанное описание правила авторизации для указанного пространства имен и псевдонима.</span><span class="sxs-lookup"><span data-stu-id="deb06-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="deb06-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="deb06-120">PARAMETERS</span></span>

### <span data-ttu-id="deb06-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="deb06-121">-AliasName</span></span>
<span data-ttu-id="deb06-122">Имя конфигурации GeoDR</span><span class="sxs-lookup"><span data-stu-id="deb06-122">GeoDR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="deb06-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deb06-123">-DefaultProfile</span></span>
<span data-ttu-id="deb06-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="deb06-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb06-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="deb06-125">-Name</span></span>
<span data-ttu-id="deb06-126">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="deb06-126">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="deb06-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="deb06-127">-Namespace</span></span>
<span data-ttu-id="deb06-128">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="deb06-128">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="deb06-129">-Очередь</span><span class="sxs-lookup"><span data-stu-id="deb06-129">-Queue</span></span>
<span data-ttu-id="deb06-130">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="deb06-130">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="deb06-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deb06-131">-ResourceGroupName</span></span>
<span data-ttu-id="deb06-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="deb06-132">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="deb06-133">-Темы</span><span class="sxs-lookup"><span data-stu-id="deb06-133">-Topic</span></span>
<span data-ttu-id="deb06-134">Название раздела</span><span class="sxs-lookup"><span data-stu-id="deb06-134">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="deb06-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb06-135">CommonParameters</span></span>
<span data-ttu-id="deb06-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="deb06-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="deb06-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deb06-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb06-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="deb06-138">INPUTS</span></span>

### <span data-ttu-id="deb06-139">System. String</span><span class="sxs-lookup"><span data-stu-id="deb06-139">System.String</span></span>


## <span data-ttu-id="deb06-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="deb06-140">OUTPUTS</span></span>

### <span data-ttu-id="deb06-141">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.5.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="deb06-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="deb06-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="deb06-142">NOTES</span></span>

## <span data-ttu-id="deb06-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="deb06-143">RELATED LINKS</span></span>
