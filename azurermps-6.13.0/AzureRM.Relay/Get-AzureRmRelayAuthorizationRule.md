---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 13de3f05879234a0db1af34517d37172c2a5a6bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734313"
---
# <span data-ttu-id="1fb81-101">Get-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1fb81-101">Get-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="1fb81-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1fb81-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb81-103">Возвращает описание указанного правила авторизации для заданных сущностей ретрансляции (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="1fb81-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fb81-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1fb81-104">SYNTAX</span></span>

### <span data-ttu-id="1fb81-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1fb81-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fb81-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1fb81-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fb81-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1fb81-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fb81-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fb81-108">DESCRIPTION</span></span>
<span data-ttu-id="1fb81-109">Командлет **Get-AzureRmRelayAuthorizationRule** получает описание указанного правила авторизации в заданных сущностях ретрансляции (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="1fb81-109">The **Get-AzureRmRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="1fb81-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1fb81-110">EXAMPLES</span></span>

### <span data-ttu-id="1fb81-111">Пример 1 — пространство имен</span><span class="sxs-lookup"><span data-stu-id="1fb81-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="1fb81-112">Возвращает указанное описание правила авторизации для указанного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1fb81-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="1fb81-113">Пример 2 — WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1fb81-113">Example 2 - WcfRelay</span></span>
```
PS C:\>Get-AzureRmWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="1fb81-114">Возвращает указанное описание правила авторизации для данного WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="1fb81-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="1fb81-115">Пример 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1fb81-115">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="1fb81-116">Возвращает указанное описание правила авторизации для данного HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="1fb81-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="1fb81-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1fb81-117">PARAMETERS</span></span>

### <span data-ttu-id="1fb81-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb81-118">-DefaultProfile</span></span>
<span data-ttu-id="1fb81-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb81-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fb81-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1fb81-120">-HybridConnection</span></span>
<span data-ttu-id="1fb81-121">HybridConnection имя.</span><span class="sxs-lookup"><span data-stu-id="1fb81-121">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb81-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1fb81-122">-Name</span></span>
<span data-ttu-id="1fb81-123">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="1fb81-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb81-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1fb81-124">-Namespace</span></span>
<span data-ttu-id="1fb81-125">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1fb81-125">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb81-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fb81-126">-ResourceGroupName</span></span>
<span data-ttu-id="1fb81-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1fb81-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="1fb81-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1fb81-128">-WcfRelay</span></span>
<span data-ttu-id="1fb81-129">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="1fb81-129">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb81-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb81-130">CommonParameters</span></span>
<span data-ttu-id="1fb81-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1fb81-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1fb81-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fb81-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb81-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1fb81-133">INPUTS</span></span>

### <span data-ttu-id="1fb81-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1fb81-134">System.String</span></span>


## <span data-ttu-id="1fb81-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fb81-135">OUTPUTS</span></span>

### <span data-ttu-id="1fb81-136">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="1fb81-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="1fb81-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="1fb81-137">NOTES</span></span>

## <span data-ttu-id="1fb81-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fb81-138">RELATED LINKS</span></span>
