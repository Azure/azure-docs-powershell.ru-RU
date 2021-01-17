---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: f99330a7611964e8db3d41f4ece56bb247c1c403
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421127"
---
# <span data-ttu-id="3d0ac-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3d0ac-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="3d0ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d0ac-102">SYNOPSIS</span></span>
<span data-ttu-id="3d0ac-103">Удаляет правило авторизации hybridConnection для заданной сущности Relay (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="3d0ac-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="3d0ac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3d0ac-104">SYNTAX</span></span>

### <span data-ttu-id="3d0ac-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3d0ac-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d0ac-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d0ac-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d0ac-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d0ac-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d0ac-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d0ac-108">DESCRIPTION</span></span>
<span data-ttu-id="3d0ac-109">Командлет **Remove-AzRelayAuthorizationRule** удаляет правило авторизации для заданной сущности Relay (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="3d0ac-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="3d0ac-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3d0ac-110">EXAMPLES</span></span>

### <span data-ttu-id="3d0ac-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3d0ac-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="3d0ac-112">Удаляет правило авторизации `AuthoRule1` пространства `TestNameSpace-Relay1` имен.</span><span class="sxs-lookup"><span data-stu-id="3d0ac-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="3d0ac-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3d0ac-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="3d0ac-114">Удаляет правило авторизации `AuthoRule1` WcfRelay `TestWcfRelay` из пространства `TestNameSpace-Relay1` имен.</span><span class="sxs-lookup"><span data-stu-id="3d0ac-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="3d0ac-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3d0ac-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="3d0ac-116">Удаляет правило авторизации `AuthoRule1` HybridConnection `TestHybridConnection` из пространства `TestNameSpace-Relay1` имен.</span><span class="sxs-lookup"><span data-stu-id="3d0ac-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="3d0ac-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d0ac-117">PARAMETERS</span></span>

### <span data-ttu-id="3d0ac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d0ac-118">-DefaultProfile</span></span>
<span data-ttu-id="3d0ac-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d0ac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d0ac-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3d0ac-120">-Force</span></span>
<span data-ttu-id="3d0ac-121">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="3d0ac-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3d0ac-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3d0ac-122">-HybridConnection</span></span>
<span data-ttu-id="3d0ac-123">Имя HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="3d0ac-123">HybridConnection Name.</span></span>

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

### <span data-ttu-id="3d0ac-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3d0ac-124">-Name</span></span>
<span data-ttu-id="3d0ac-125">Имяrule authorizationRule.</span><span class="sxs-lookup"><span data-stu-id="3d0ac-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="3d0ac-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3d0ac-126">-Namespace</span></span>
<span data-ttu-id="3d0ac-127">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3d0ac-127">Namespace Name.</span></span>

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

### <span data-ttu-id="3d0ac-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d0ac-128">-PassThru</span></span>
<span data-ttu-id="3d0ac-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3d0ac-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3d0ac-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d0ac-130">-ResourceGroupName</span></span>
<span data-ttu-id="3d0ac-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3d0ac-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="3d0ac-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3d0ac-132">-WcfRelay</span></span>
<span data-ttu-id="3d0ac-133">Имя WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="3d0ac-133">WcfRelay Name.</span></span>

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

### <span data-ttu-id="3d0ac-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d0ac-134">-Confirm</span></span>
<span data-ttu-id="3d0ac-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3d0ac-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d0ac-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d0ac-136">-WhatIf</span></span>
<span data-ttu-id="3d0ac-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d0ac-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d0ac-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3d0ac-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d0ac-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d0ac-139">CommonParameters</span></span>
<span data-ttu-id="3d0ac-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d0ac-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d0ac-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d0ac-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d0ac-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d0ac-142">INPUTS</span></span>

### <span data-ttu-id="3d0ac-143">System.String</span><span class="sxs-lookup"><span data-stu-id="3d0ac-143">System.String</span></span>

## <span data-ttu-id="3d0ac-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3d0ac-144">OUTPUTS</span></span>

### <span data-ttu-id="3d0ac-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3d0ac-145">System.Boolean</span></span>

## <span data-ttu-id="3d0ac-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3d0ac-146">NOTES</span></span>

## <span data-ttu-id="3d0ac-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d0ac-147">RELATED LINKS</span></span>
