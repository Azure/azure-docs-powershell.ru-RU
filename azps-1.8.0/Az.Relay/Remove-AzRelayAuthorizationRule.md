---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: 8523fd6698e2fcdc4212b68a93269d60bc642628
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729501"
---
# <span data-ttu-id="42e48-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="42e48-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="42e48-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42e48-102">SYNOPSIS</span></span>
<span data-ttu-id="42e48-103">Удаляет правило авторизации HybridConnection из заданных сущностей ретрансляции (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="42e48-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="42e48-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42e48-104">SYNTAX</span></span>

### <span data-ttu-id="42e48-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="42e48-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42e48-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="42e48-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42e48-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="42e48-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42e48-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42e48-108">DESCRIPTION</span></span>
<span data-ttu-id="42e48-109">Командлет **Remove-AzRelayAuthorizationRule** удаляет правило авторизации для заданных сущностей ретрансляции (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="42e48-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="42e48-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42e48-110">EXAMPLES</span></span>

### <span data-ttu-id="42e48-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="42e48-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="42e48-112">Удаляет правило авторизации `AuthoRule1` для пространства имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="42e48-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="42e48-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="42e48-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="42e48-114">Удаляет правило авторизации `AuthoRule1` WcfRelay `TestWcfRelay` из пространства имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="42e48-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="42e48-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="42e48-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="42e48-116">Удаляет правило авторизации `AuthoRule1` HybridConnection `TestHybridConnection` из пространства имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="42e48-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="42e48-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42e48-117">PARAMETERS</span></span>

### <span data-ttu-id="42e48-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e48-118">-DefaultProfile</span></span>
<span data-ttu-id="42e48-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42e48-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42e48-120">-Force</span><span class="sxs-lookup"><span data-stu-id="42e48-120">-Force</span></span>
<span data-ttu-id="42e48-121">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="42e48-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="42e48-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="42e48-122">-HybridConnection</span></span>
<span data-ttu-id="42e48-123">HybridConnection имя.</span><span class="sxs-lookup"><span data-stu-id="42e48-123">HybridConnection Name.</span></span>

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

### <span data-ttu-id="42e48-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="42e48-124">-Name</span></span>
<span data-ttu-id="42e48-125">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="42e48-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="42e48-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="42e48-126">-Namespace</span></span>
<span data-ttu-id="42e48-127">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="42e48-127">Namespace Name.</span></span>

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

### <span data-ttu-id="42e48-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42e48-128">-PassThru</span></span>
<span data-ttu-id="42e48-129">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="42e48-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="42e48-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42e48-130">-ResourceGroupName</span></span>
<span data-ttu-id="42e48-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="42e48-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="42e48-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="42e48-132">-WcfRelay</span></span>
<span data-ttu-id="42e48-133">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="42e48-133">WcfRelay Name.</span></span>

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

### <span data-ttu-id="42e48-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42e48-134">-Confirm</span></span>
<span data-ttu-id="42e48-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="42e48-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42e48-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42e48-136">-WhatIf</span></span>
<span data-ttu-id="42e48-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="42e48-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42e48-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="42e48-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42e48-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e48-139">CommonParameters</span></span>
<span data-ttu-id="42e48-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42e48-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e48-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42e48-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e48-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42e48-142">INPUTS</span></span>

### <span data-ttu-id="42e48-143">System. String</span><span class="sxs-lookup"><span data-stu-id="42e48-143">System.String</span></span>

## <span data-ttu-id="42e48-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42e48-144">OUTPUTS</span></span>

### <span data-ttu-id="42e48-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42e48-145">System.Boolean</span></span>

## <span data-ttu-id="42e48-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="42e48-146">NOTES</span></span>

## <span data-ttu-id="42e48-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42e48-147">RELATED LINKS</span></span>
