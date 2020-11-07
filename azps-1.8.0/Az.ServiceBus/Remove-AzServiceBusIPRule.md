---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
ms.openlocfilehash: 3fc71bb4e460cb7763fc437f0bc2ac31860dccdf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729170"
---
# <span data-ttu-id="1f348-101">Remove-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="1f348-101">Remove-AzServiceBusIPRule</span></span>

## <span data-ttu-id="1f348-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f348-102">SYNOPSIS</span></span>
<span data-ttu-id="1f348-103">Удаление одного IPrule для NetworkRuleSet из заданного пространства имен</span><span class="sxs-lookup"><span data-stu-id="1f348-103">Remove a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="1f348-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f348-104">SYNTAX</span></span>

### <span data-ttu-id="1f348-105">IPRulePropertiesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1f348-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f348-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f348-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f348-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f348-107">DESCRIPTION</span></span>
<span data-ttu-id="1f348-108">Удаление одного IPrule для NetworkRuleSet из заданного пространства имен</span><span class="sxs-lookup"><span data-stu-id="1f348-108">Remove a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="1f348-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f348-109">EXAMPLES</span></span>

### <span data-ttu-id="1f348-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1f348-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="1f348-111">Удаляет IpMask из NetworkRuleSet заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1f348-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="1f348-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f348-112">PARAMETERS</span></span>

### <span data-ttu-id="1f348-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f348-113">-AsJob</span></span>
<span data-ttu-id="1f348-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1f348-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f348-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f348-115">-DefaultProfile</span></span>
<span data-ttu-id="1f348-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f348-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f348-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="1f348-117">-IpMask</span></span>
<span data-ttu-id="1f348-118">Идентификатор ресурса подсети</span><span class="sxs-lookup"><span data-stu-id="1f348-118">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f348-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="1f348-119">-IpRuleObject</span></span>
<span data-ttu-id="1f348-120">Объект конфигурации IPRule</span><span class="sxs-lookup"><span data-stu-id="1f348-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f348-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1f348-121">-Name</span></span>
<span data-ttu-id="1f348-122">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="1f348-122">Namespace Name</span></span>

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

### <span data-ttu-id="1f348-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f348-123">-PassThru</span></span>
<span data-ttu-id="1f348-124">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="1f348-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1f348-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f348-125">-ResourceGroupName</span></span>
<span data-ttu-id="1f348-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1f348-126">Resource Group Name</span></span>

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

### <span data-ttu-id="1f348-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f348-127">-Confirm</span></span>
<span data-ttu-id="1f348-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1f348-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f348-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f348-129">-WhatIf</span></span>
<span data-ttu-id="1f348-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1f348-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f348-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1f348-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f348-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f348-132">CommonParameters</span></span>
<span data-ttu-id="1f348-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f348-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1f348-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f348-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f348-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f348-135">INPUTS</span></span>

### <span data-ttu-id="1f348-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1f348-136">System.String</span></span>

### <span data-ttu-id="1f348-137">Microsoft. Azure. Commands. ServiceBus. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="1f348-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="1f348-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f348-138">OUTPUTS</span></span>

### <span data-ttu-id="1f348-139">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="1f348-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="1f348-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f348-140">NOTES</span></span>

## <span data-ttu-id="1f348-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f348-141">RELATED LINKS</span></span>
