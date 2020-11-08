---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
ms.openlocfilehash: af83820d33b9f36d93cc7623001d22a6cb5e0212
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235921"
---
# <span data-ttu-id="41f82-101">Get-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="41f82-101">Get-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="41f82-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41f82-102">SYNOPSIS</span></span>
<span data-ttu-id="41f82-103">Возвращает описание указанного правила авторизации для заданных сущностей ретрансляции (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="41f82-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="41f82-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41f82-104">SYNTAX</span></span>

### <span data-ttu-id="41f82-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="41f82-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41f82-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="41f82-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41f82-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="41f82-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41f82-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41f82-108">DESCRIPTION</span></span>
<span data-ttu-id="41f82-109">Командлет **Get-AzRelayAuthorizationRule** получает описание указанного правила авторизации в заданных сущностях ретрансляции (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="41f82-109">The **Get-AzRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="41f82-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41f82-110">EXAMPLES</span></span>

### <span data-ttu-id="41f82-111">Пример 1: пространство имен</span><span class="sxs-lookup"><span data-stu-id="41f82-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="41f82-112">Возвращает указанное описание правила авторизации для указанного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="41f82-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="41f82-113">Пример 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="41f82-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>Get-AzWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="41f82-114">Возвращает указанное описание правила авторизации для данного WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="41f82-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="41f82-115">Пример 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="41f82-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="41f82-116">Возвращает указанное описание правила авторизации для данного HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="41f82-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="41f82-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41f82-117">PARAMETERS</span></span>

### <span data-ttu-id="41f82-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41f82-118">-DefaultProfile</span></span>
<span data-ttu-id="41f82-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41f82-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41f82-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="41f82-120">-HybridConnection</span></span>
<span data-ttu-id="41f82-121">HybridConnection имя.</span><span class="sxs-lookup"><span data-stu-id="41f82-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="41f82-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="41f82-122">-Name</span></span>
<span data-ttu-id="41f82-123">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="41f82-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="41f82-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="41f82-124">-Namespace</span></span>
<span data-ttu-id="41f82-125">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="41f82-125">Namespace Name.</span></span>

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

### <span data-ttu-id="41f82-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41f82-126">-ResourceGroupName</span></span>
<span data-ttu-id="41f82-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41f82-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="41f82-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="41f82-128">-WcfRelay</span></span>
<span data-ttu-id="41f82-129">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="41f82-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="41f82-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41f82-130">CommonParameters</span></span>
<span data-ttu-id="41f82-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41f82-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41f82-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41f82-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41f82-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41f82-133">INPUTS</span></span>

### <span data-ttu-id="41f82-134">System. String</span><span class="sxs-lookup"><span data-stu-id="41f82-134">System.String</span></span>

## <span data-ttu-id="41f82-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41f82-135">OUTPUTS</span></span>

### <span data-ttu-id="41f82-136">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="41f82-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="41f82-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="41f82-137">NOTES</span></span>

## <span data-ttu-id="41f82-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41f82-138">RELATED LINKS</span></span>
