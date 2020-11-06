---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: 96b95a4a6641e3bcfc2c1a18653da4231bee5c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558267"
---
# <span data-ttu-id="595d8-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="595d8-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="595d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="595d8-102">SYNOPSIS</span></span>
<span data-ttu-id="595d8-103">Получает первичные и дополнительные строки подключения для заданного пространства имен, очереди или темы или псевдонима (конфигурации GeoDR).</span><span class="sxs-lookup"><span data-stu-id="595d8-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="595d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="595d8-104">SYNTAX</span></span>

### <span data-ttu-id="595d8-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="595d8-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="595d8-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="595d8-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="595d8-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="595d8-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="595d8-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="595d8-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="595d8-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="595d8-109">DESCRIPTION</span></span>
<span data-ttu-id="595d8-110">Командлет **Get-AzureRmServiceBusKey** возвращает первичные и дополнительные строки подключения для данного пространства имен, очереди или темы или псевдонима (конфигурации GeoDR).</span><span class="sxs-lookup"><span data-stu-id="595d8-110">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="595d8-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="595d8-111">EXAMPLES</span></span>

### <span data-ttu-id="595d8-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="595d8-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="595d8-113">Основной и дополнительный строки подключения к указанному пространству имен.</span><span class="sxs-lookup"><span data-stu-id="595d8-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="595d8-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="595d8-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="595d8-115">Основной и дополнительный строки подключения к указанной очереди.</span><span class="sxs-lookup"><span data-stu-id="595d8-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="595d8-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="595d8-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="595d8-117">Основной и дополнительный строки соединения с указанным разделом.</span><span class="sxs-lookup"><span data-stu-id="595d8-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="595d8-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="595d8-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="595d8-119">Основной и дополнительный строки соединения с указанным пространством имен и псевдонимом.</span><span class="sxs-lookup"><span data-stu-id="595d8-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="595d8-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="595d8-120">PARAMETERS</span></span>

### <span data-ttu-id="595d8-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="595d8-121">-AliasName</span></span>
<span data-ttu-id="595d8-122">Имя псевдонима</span><span class="sxs-lookup"><span data-stu-id="595d8-122">Alias Name</span></span>

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

### <span data-ttu-id="595d8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="595d8-123">-DefaultProfile</span></span>
<span data-ttu-id="595d8-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="595d8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="595d8-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="595d8-125">-Name</span></span>
<span data-ttu-id="595d8-126">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="595d8-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="595d8-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="595d8-127">-Namespace</span></span>
<span data-ttu-id="595d8-128">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="595d8-128">Namespace Name</span></span>

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

### <span data-ttu-id="595d8-129">-Очередь</span><span class="sxs-lookup"><span data-stu-id="595d8-129">-Queue</span></span>
<span data-ttu-id="595d8-130">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="595d8-130">Queue Name</span></span>

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

### <span data-ttu-id="595d8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="595d8-131">-ResourceGroupName</span></span>
<span data-ttu-id="595d8-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="595d8-132">Resource Group Name</span></span>

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

### <span data-ttu-id="595d8-133">-Темы</span><span class="sxs-lookup"><span data-stu-id="595d8-133">-Topic</span></span>
<span data-ttu-id="595d8-134">Название раздела</span><span class="sxs-lookup"><span data-stu-id="595d8-134">Topic Name</span></span>

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

### <span data-ttu-id="595d8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="595d8-135">CommonParameters</span></span>
<span data-ttu-id="595d8-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="595d8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="595d8-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="595d8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="595d8-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="595d8-138">INPUTS</span></span>

### <span data-ttu-id="595d8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="595d8-139">System.String</span></span>

## <span data-ttu-id="595d8-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="595d8-140">OUTPUTS</span></span>

### <span data-ttu-id="595d8-141">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="595d8-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="595d8-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="595d8-142">NOTES</span></span>

## <span data-ttu-id="595d8-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="595d8-143">RELATED LINKS</span></span>
