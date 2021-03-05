---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: 1284780428fdaacfc255faf2ac640565eec44950
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000483"
---
# <span data-ttu-id="5ea5c-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5ea5c-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="5ea5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ea5c-102">SYNOPSIS</span></span>
<span data-ttu-id="5ea5c-103">Удаляет правило авторизации гибридной связи для заданной сущности Relay (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="5ea5c-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="5ea5c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5ea5c-104">SYNTAX</span></span>

### <span data-ttu-id="5ea5c-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5ea5c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ea5c-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5ea5c-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ea5c-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5ea5c-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ea5c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ea5c-108">DESCRIPTION</span></span>
<span data-ttu-id="5ea5c-109">Командлет **Remove-AzRelayAuthorizationRule** удаляет правило авторизации для заданной сущности Relay (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="5ea5c-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="5ea5c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5ea5c-110">EXAMPLES</span></span>

### <span data-ttu-id="5ea5c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5ea5c-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="5ea5c-112">Удаляет правило авторизации `AuthoRule1` пространства `TestNameSpace-Relay1` имен.</span><span class="sxs-lookup"><span data-stu-id="5ea5c-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="5ea5c-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5ea5c-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="5ea5c-114">Удаляет правило авторизации `AuthoRule1` WcfRelay `TestWcfRelay` из пространства `TestNameSpace-Relay1` имен.</span><span class="sxs-lookup"><span data-stu-id="5ea5c-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="5ea5c-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5ea5c-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="5ea5c-116">Удаляет правило авторизации `AuthoRule1` HybridConnection `TestHybridConnection` из пространства `TestNameSpace-Relay1` имен.</span><span class="sxs-lookup"><span data-stu-id="5ea5c-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="5ea5c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ea5c-117">PARAMETERS</span></span>

### <span data-ttu-id="5ea5c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ea5c-118">-DefaultProfile</span></span>
<span data-ttu-id="5ea5c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ea5c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ea5c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5ea5c-120">-Force</span></span>
<span data-ttu-id="5ea5c-121">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="5ea5c-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ea5c-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="5ea5c-122">-HybridConnection</span></span>
<span data-ttu-id="5ea5c-123">Имя HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="5ea5c-123">HybridConnection Name.</span></span>

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

### <span data-ttu-id="5ea5c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5ea5c-124">-Name</span></span>
<span data-ttu-id="5ea5c-125">Имяrule authorizationRule.</span><span class="sxs-lookup"><span data-stu-id="5ea5c-125">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ea5c-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5ea5c-126">-Namespace</span></span>
<span data-ttu-id="5ea5c-127">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="5ea5c-127">Namespace Name.</span></span>

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

### <span data-ttu-id="5ea5c-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ea5c-128">-PassThru</span></span>
<span data-ttu-id="5ea5c-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5ea5c-129">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ea5c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ea5c-130">-ResourceGroupName</span></span>
<span data-ttu-id="5ea5c-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5ea5c-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="5ea5c-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="5ea5c-132">-WcfRelay</span></span>
<span data-ttu-id="5ea5c-133">Имя WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="5ea5c-133">WcfRelay Name.</span></span>

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

### <span data-ttu-id="5ea5c-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ea5c-134">-Confirm</span></span>
<span data-ttu-id="5ea5c-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5ea5c-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ea5c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ea5c-136">-WhatIf</span></span>
<span data-ttu-id="5ea5c-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ea5c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ea5c-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5ea5c-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ea5c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ea5c-139">CommonParameters</span></span>
<span data-ttu-id="5ea5c-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ea5c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ea5c-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ea5c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ea5c-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ea5c-142">INPUTS</span></span>

### <span data-ttu-id="5ea5c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="5ea5c-143">System.String</span></span>

## <span data-ttu-id="5ea5c-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5ea5c-144">OUTPUTS</span></span>

### <span data-ttu-id="5ea5c-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5ea5c-145">System.Boolean</span></span>

## <span data-ttu-id="5ea5c-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5ea5c-146">NOTES</span></span>

## <span data-ttu-id="5ea5c-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ea5c-147">RELATED LINKS</span></span>
