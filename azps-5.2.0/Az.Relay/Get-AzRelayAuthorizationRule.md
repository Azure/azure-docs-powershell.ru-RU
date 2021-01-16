---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
ms.openlocfilehash: af83820d33b9f36d93cc7623001d22a6cb5e0212
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409172"
---
# <span data-ttu-id="e39a7-101">Get-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e39a7-101">Get-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="e39a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e39a7-102">SYNOPSIS</span></span>
<span data-ttu-id="e39a7-103">Описание заданного правила авторизации для определенных сущностями Relay (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="e39a7-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="e39a7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e39a7-104">SYNTAX</span></span>

### <span data-ttu-id="e39a7-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e39a7-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e39a7-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e39a7-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e39a7-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e39a7-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e39a7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e39a7-108">DESCRIPTION</span></span>
<span data-ttu-id="e39a7-109">Командлет **Get-AzRelayAuthorizationRule** получает описание указанного правила авторизации в указанных сущности Relay (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="e39a7-109">The **Get-AzRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="e39a7-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e39a7-110">EXAMPLES</span></span>

### <span data-ttu-id="e39a7-111">Пример 1. Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e39a7-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="e39a7-112">Возвращает описание указанного правила авторизации для указанного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="e39a7-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="e39a7-113">Пример 2. WcfRelay</span><span class="sxs-lookup"><span data-stu-id="e39a7-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>Get-AzWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="e39a7-114">Возвращает описание заданного правила авторизации для данного WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="e39a7-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="e39a7-115">Пример 3. Гибриднаясоединение</span><span class="sxs-lookup"><span data-stu-id="e39a7-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="e39a7-116">Возвращает описание заданного правила авторизации для данного гибридного подключения.</span><span class="sxs-lookup"><span data-stu-id="e39a7-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="e39a7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e39a7-117">PARAMETERS</span></span>

### <span data-ttu-id="e39a7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e39a7-118">-DefaultProfile</span></span>
<span data-ttu-id="e39a7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e39a7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e39a7-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="e39a7-120">-HybridConnection</span></span>
<span data-ttu-id="e39a7-121">Имя HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="e39a7-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="e39a7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e39a7-122">-Name</span></span>
<span data-ttu-id="e39a7-123">Имяrule authorizationRule.</span><span class="sxs-lookup"><span data-stu-id="e39a7-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="e39a7-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e39a7-124">-Namespace</span></span>
<span data-ttu-id="e39a7-125">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="e39a7-125">Namespace Name.</span></span>

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

### <span data-ttu-id="e39a7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e39a7-126">-ResourceGroupName</span></span>
<span data-ttu-id="e39a7-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e39a7-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="e39a7-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="e39a7-128">-WcfRelay</span></span>
<span data-ttu-id="e39a7-129">Имя WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="e39a7-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="e39a7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e39a7-130">CommonParameters</span></span>
<span data-ttu-id="e39a7-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e39a7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e39a7-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e39a7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e39a7-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e39a7-133">INPUTS</span></span>

### <span data-ttu-id="e39a7-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e39a7-134">System.String</span></span>

## <span data-ttu-id="e39a7-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e39a7-135">OUTPUTS</span></span>

### <span data-ttu-id="e39a7-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e39a7-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e39a7-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e39a7-137">NOTES</span></span>

## <span data-ttu-id="e39a7-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e39a7-138">RELATED LINKS</span></span>
