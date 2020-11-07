---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
ms.openlocfilehash: f159e3d82aa93f4b3bf663f6bff6e8ede599e860
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905354"
---
# <span data-ttu-id="6c9f9-101">Remove-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="6c9f9-101">Remove-AzServiceBusIPRule</span></span>

## <span data-ttu-id="6c9f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6c9f9-102">SYNOPSIS</span></span>
<span data-ttu-id="6c9f9-103">Удаление отдельного правила IP-адреса для NetworkRuleSet заданного пространства имен</span><span class="sxs-lookup"><span data-stu-id="6c9f9-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="6c9f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6c9f9-104">SYNTAX</span></span>

### <span data-ttu-id="6c9f9-105">IPRulePropertiesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6c9f9-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c9f9-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c9f9-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c9f9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c9f9-107">DESCRIPTION</span></span>
<span data-ttu-id="6c9f9-108">Удаление отдельного правила IP-адреса для NetworkRuleSet заданного пространства имен</span><span class="sxs-lookup"><span data-stu-id="6c9f9-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="6c9f9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6c9f9-109">EXAMPLES</span></span>

### <span data-ttu-id="6c9f9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6c9f9-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="6c9f9-111">Удаляет IpMask из NetworkRuleSet заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="6c9f9-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="6c9f9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6c9f9-112">PARAMETERS</span></span>

### <span data-ttu-id="6c9f9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c9f9-113">-AsJob</span></span>
<span data-ttu-id="6c9f9-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6c9f9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c9f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c9f9-115">-DefaultProfile</span></span>
<span data-ttu-id="6c9f9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c9f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c9f9-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="6c9f9-117">-IpMask</span></span>
<span data-ttu-id="6c9f9-118">Идентификатор ресурса подсети</span><span class="sxs-lookup"><span data-stu-id="6c9f9-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="6c9f9-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="6c9f9-119">-IpRuleObject</span></span>
<span data-ttu-id="6c9f9-120">Объект конфигурации IPRule</span><span class="sxs-lookup"><span data-stu-id="6c9f9-120">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="6c9f9-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6c9f9-121">-Name</span></span>
<span data-ttu-id="6c9f9-122">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="6c9f9-122">Namespace Name</span></span>

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

### <span data-ttu-id="6c9f9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c9f9-123">-PassThru</span></span>
<span data-ttu-id="6c9f9-124">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="6c9f9-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6c9f9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c9f9-125">-ResourceGroupName</span></span>
<span data-ttu-id="6c9f9-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6c9f9-126">Resource Group Name</span></span>

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

### <span data-ttu-id="6c9f9-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c9f9-127">-Confirm</span></span>
<span data-ttu-id="6c9f9-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6c9f9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c9f9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c9f9-129">-WhatIf</span></span>
<span data-ttu-id="6c9f9-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6c9f9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c9f9-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6c9f9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c9f9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c9f9-132">CommonParameters</span></span>
<span data-ttu-id="6c9f9-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6c9f9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6c9f9-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c9f9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c9f9-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6c9f9-135">INPUTS</span></span>

### <span data-ttu-id="6c9f9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6c9f9-136">System.String</span></span>

### <span data-ttu-id="6c9f9-137">Microsoft. Azure. Commands. ServiceBus. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="6c9f9-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="6c9f9-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c9f9-138">OUTPUTS</span></span>

### <span data-ttu-id="6c9f9-139">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="6c9f9-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="6c9f9-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="6c9f9-140">NOTES</span></span>

## <span data-ttu-id="6c9f9-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c9f9-141">RELATED LINKS</span></span>
