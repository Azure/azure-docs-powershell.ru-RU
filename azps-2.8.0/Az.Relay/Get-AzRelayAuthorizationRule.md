---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
ms.openlocfilehash: 18798e0153bd36e26a9f98027c95cbacf80d7ee4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904190"
---
# <span data-ttu-id="f81c8-101">Get-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f81c8-101">Get-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="f81c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f81c8-102">SYNOPSIS</span></span>
<span data-ttu-id="f81c8-103">Возвращает описание указанного правила авторизации для заданных сущностей ретрансляции (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="f81c8-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f81c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f81c8-104">SYNTAX</span></span>

### <span data-ttu-id="f81c8-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f81c8-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f81c8-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f81c8-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f81c8-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f81c8-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f81c8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f81c8-108">DESCRIPTION</span></span>
<span data-ttu-id="f81c8-109">Командлет **Get-AzRelayAuthorizationRule** получает описание указанного правила авторизации в заданных сущностях ретрансляции (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="f81c8-109">The **Get-AzRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f81c8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f81c8-110">EXAMPLES</span></span>

### <span data-ttu-id="f81c8-111">Пример 1 — пространство имен</span><span class="sxs-lookup"><span data-stu-id="f81c8-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="f81c8-112">Возвращает указанное описание правила авторизации для указанного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f81c8-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="f81c8-113">Пример 2 — WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f81c8-113">Example 2 - WcfRelay</span></span>
```
PS C:\>Get-AzWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="f81c8-114">Возвращает указанное описание правила авторизации для данного WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="f81c8-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="f81c8-115">Пример 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f81c8-115">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="f81c8-116">Возвращает указанное описание правила авторизации для данного HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="f81c8-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="f81c8-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f81c8-117">PARAMETERS</span></span>

### <span data-ttu-id="f81c8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f81c8-118">-DefaultProfile</span></span>
<span data-ttu-id="f81c8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f81c8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f81c8-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f81c8-120">-HybridConnection</span></span>
<span data-ttu-id="f81c8-121">HybridConnection имя.</span><span class="sxs-lookup"><span data-stu-id="f81c8-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="f81c8-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f81c8-122">-Name</span></span>
<span data-ttu-id="f81c8-123">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="f81c8-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="f81c8-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f81c8-124">-Namespace</span></span>
<span data-ttu-id="f81c8-125">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f81c8-125">Namespace Name.</span></span>

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

### <span data-ttu-id="f81c8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f81c8-126">-ResourceGroupName</span></span>
<span data-ttu-id="f81c8-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f81c8-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="f81c8-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f81c8-128">-WcfRelay</span></span>
<span data-ttu-id="f81c8-129">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="f81c8-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="f81c8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f81c8-130">CommonParameters</span></span>
<span data-ttu-id="f81c8-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f81c8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f81c8-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f81c8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f81c8-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f81c8-133">INPUTS</span></span>

### <span data-ttu-id="f81c8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f81c8-134">System.String</span></span>

## <span data-ttu-id="f81c8-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f81c8-135">OUTPUTS</span></span>

### <span data-ttu-id="f81c8-136">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f81c8-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f81c8-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="f81c8-137">NOTES</span></span>

## <span data-ttu-id="f81c8-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f81c8-138">RELATED LINKS</span></span>
