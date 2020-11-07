---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
ms.openlocfilehash: 53358ef1afc53eed779000c7bb8912b312980784
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720934"
---
# <span data-ttu-id="977e4-101">Remove-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="977e4-101">Remove-AzEventHubIPRule</span></span>

## <span data-ttu-id="977e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="977e4-102">SYNOPSIS</span></span>
<span data-ttu-id="977e4-103">Удаление отдельного правила IP-адреса для NetworkRuleSet заданного пространства имен</span><span class="sxs-lookup"><span data-stu-id="977e4-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="977e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="977e4-104">SYNTAX</span></span>

### <span data-ttu-id="977e4-105">IPRulePropertiesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="977e4-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="977e4-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="977e4-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="977e4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="977e4-107">DESCRIPTION</span></span>
<span data-ttu-id="977e4-108">Удаление отдельного правила IP-адреса для NetworkRuleSet заданного пространства имен</span><span class="sxs-lookup"><span data-stu-id="977e4-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="977e4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="977e4-109">EXAMPLES</span></span>

### <span data-ttu-id="977e4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="977e4-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="977e4-111">Удаляет IpMask из NetworkRuleSet заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="977e4-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="977e4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="977e4-112">PARAMETERS</span></span>

### <span data-ttu-id="977e4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="977e4-113">-AsJob</span></span>
<span data-ttu-id="977e4-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="977e4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="977e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="977e4-115">-DefaultProfile</span></span>
<span data-ttu-id="977e4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="977e4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="977e4-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="977e4-117">-IpMask</span></span>
<span data-ttu-id="977e4-118">Идентификатор ресурса подсети</span><span class="sxs-lookup"><span data-stu-id="977e4-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="977e4-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="977e4-119">-IpRuleObject</span></span>
<span data-ttu-id="977e4-120">Объект конфигурации IPRule</span><span class="sxs-lookup"><span data-stu-id="977e4-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="977e4-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="977e4-121">-Name</span></span>
<span data-ttu-id="977e4-122">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="977e4-122">Namespace Name</span></span>

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

### <span data-ttu-id="977e4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="977e4-123">-PassThru</span></span>
<span data-ttu-id="977e4-124">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="977e4-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="977e4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="977e4-125">-ResourceGroupName</span></span>
<span data-ttu-id="977e4-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="977e4-126">Resource Group Name</span></span>

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

### <span data-ttu-id="977e4-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="977e4-127">-Confirm</span></span>
<span data-ttu-id="977e4-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="977e4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="977e4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="977e4-129">-WhatIf</span></span>
<span data-ttu-id="977e4-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="977e4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="977e4-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="977e4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="977e4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="977e4-132">CommonParameters</span></span>
<span data-ttu-id="977e4-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="977e4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="977e4-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="977e4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="977e4-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="977e4-135">INPUTS</span></span>

### <span data-ttu-id="977e4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="977e4-136">System.String</span></span>

### <span data-ttu-id="977e4-137">Microsoft. Azure. Commands. EventHub. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="977e4-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="977e4-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="977e4-138">OUTPUTS</span></span>

### <span data-ttu-id="977e4-139">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="977e4-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="977e4-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="977e4-140">NOTES</span></span>

## <span data-ttu-id="977e4-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="977e4-141">RELATED LINKS</span></span>