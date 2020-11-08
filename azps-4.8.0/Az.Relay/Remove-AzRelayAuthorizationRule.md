---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: f99330a7611964e8db3d41f4ece56bb247c1c403
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079355"
---
# <span data-ttu-id="9ae4e-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9ae4e-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="9ae4e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ae4e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ae4e-103">Удаляет правило авторизации HybridConnection из заданных сущностей ретрансляции (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="9ae4e-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="9ae4e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ae4e-104">SYNTAX</span></span>

### <span data-ttu-id="9ae4e-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ae4e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ae4e-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9ae4e-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ae4e-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9ae4e-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ae4e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ae4e-108">DESCRIPTION</span></span>
<span data-ttu-id="9ae4e-109">Командлет **Remove-AzRelayAuthorizationRule** удаляет правило авторизации для заданных сущностей ретрансляции (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="9ae4e-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="9ae4e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ae4e-110">EXAMPLES</span></span>

### <span data-ttu-id="9ae4e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9ae4e-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="9ae4e-112">Удаляет правило авторизации `AuthoRule1` для пространства имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="9ae4e-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="9ae4e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9ae4e-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="9ae4e-114">Удаляет правило авторизации `AuthoRule1` WcfRelay `TestWcfRelay` из пространства имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="9ae4e-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="9ae4e-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="9ae4e-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="9ae4e-116">Удаляет правило авторизации `AuthoRule1` HybridConnection `TestHybridConnection` из пространства имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="9ae4e-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="9ae4e-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ae4e-117">PARAMETERS</span></span>

### <span data-ttu-id="9ae4e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ae4e-118">-DefaultProfile</span></span>
<span data-ttu-id="9ae4e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae4e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ae4e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9ae4e-120">-Force</span></span>
<span data-ttu-id="9ae4e-121">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9ae4e-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9ae4e-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="9ae4e-122">-HybridConnection</span></span>
<span data-ttu-id="9ae4e-123">HybridConnection имя.</span><span class="sxs-lookup"><span data-stu-id="9ae4e-123">HybridConnection Name.</span></span>

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

### <span data-ttu-id="9ae4e-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9ae4e-124">-Name</span></span>
<span data-ttu-id="9ae4e-125">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="9ae4e-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="9ae4e-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9ae4e-126">-Namespace</span></span>
<span data-ttu-id="9ae4e-127">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="9ae4e-127">Namespace Name.</span></span>

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

### <span data-ttu-id="9ae4e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ae4e-128">-PassThru</span></span>
<span data-ttu-id="9ae4e-129">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="9ae4e-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9ae4e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ae4e-130">-ResourceGroupName</span></span>
<span data-ttu-id="9ae4e-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ae4e-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="9ae4e-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="9ae4e-132">-WcfRelay</span></span>
<span data-ttu-id="9ae4e-133">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="9ae4e-133">WcfRelay Name.</span></span>

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

### <span data-ttu-id="9ae4e-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ae4e-134">-Confirm</span></span>
<span data-ttu-id="9ae4e-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9ae4e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ae4e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ae4e-136">-WhatIf</span></span>
<span data-ttu-id="9ae4e-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9ae4e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ae4e-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9ae4e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ae4e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ae4e-139">CommonParameters</span></span>
<span data-ttu-id="9ae4e-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ae4e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ae4e-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ae4e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ae4e-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ae4e-142">INPUTS</span></span>

### <span data-ttu-id="9ae4e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9ae4e-143">System.String</span></span>

## <span data-ttu-id="9ae4e-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ae4e-144">OUTPUTS</span></span>

### <span data-ttu-id="9ae4e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ae4e-145">System.Boolean</span></span>

## <span data-ttu-id="9ae4e-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ae4e-146">NOTES</span></span>

## <span data-ttu-id="9ae4e-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ae4e-147">RELATED LINKS</span></span>