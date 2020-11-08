---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
ms.openlocfilehash: 00213d4829d4b389f19a01ad9748517608657136
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242778"
---
# <span data-ttu-id="9bfad-101">Remove-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="9bfad-101">Remove-AzEventHubIPRule</span></span>

## <span data-ttu-id="9bfad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9bfad-102">SYNOPSIS</span></span>
<span data-ttu-id="9bfad-103">Удаление отдельного правила IP-адреса для NetworkRuleSet заданного пространства имен</span><span class="sxs-lookup"><span data-stu-id="9bfad-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="9bfad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9bfad-104">SYNTAX</span></span>

### <span data-ttu-id="9bfad-105">IPRulePropertiesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9bfad-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bfad-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bfad-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9bfad-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bfad-107">DESCRIPTION</span></span>
<span data-ttu-id="9bfad-108">Удаление отдельного правила IP-адреса для NetworkRuleSet заданного пространства имен</span><span class="sxs-lookup"><span data-stu-id="9bfad-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="9bfad-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9bfad-109">EXAMPLES</span></span>

### <span data-ttu-id="9bfad-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9bfad-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="9bfad-111">Удаляет IpMask из NetworkRuleSet заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="9bfad-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="9bfad-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9bfad-112">PARAMETERS</span></span>

### <span data-ttu-id="9bfad-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9bfad-113">-AsJob</span></span>
<span data-ttu-id="9bfad-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9bfad-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9bfad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bfad-115">-DefaultProfile</span></span>
<span data-ttu-id="9bfad-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9bfad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bfad-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="9bfad-117">-IpMask</span></span>
<span data-ttu-id="9bfad-118">Идентификатор ресурса подсети</span><span class="sxs-lookup"><span data-stu-id="9bfad-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="9bfad-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="9bfad-119">-IpRuleObject</span></span>
<span data-ttu-id="9bfad-120">Объект конфигурации IPRule</span><span class="sxs-lookup"><span data-stu-id="9bfad-120">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="9bfad-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9bfad-121">-Name</span></span>
<span data-ttu-id="9bfad-122">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="9bfad-122">Namespace Name</span></span>

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

### <span data-ttu-id="9bfad-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9bfad-123">-PassThru</span></span>
<span data-ttu-id="9bfad-124">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="9bfad-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9bfad-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bfad-125">-ResourceGroupName</span></span>
<span data-ttu-id="9bfad-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9bfad-126">Resource Group Name</span></span>

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

### <span data-ttu-id="9bfad-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9bfad-127">-Confirm</span></span>
<span data-ttu-id="9bfad-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9bfad-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bfad-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bfad-129">-WhatIf</span></span>
<span data-ttu-id="9bfad-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9bfad-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bfad-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9bfad-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bfad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bfad-132">CommonParameters</span></span>
<span data-ttu-id="9bfad-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9bfad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9bfad-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bfad-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bfad-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9bfad-135">INPUTS</span></span>

### <span data-ttu-id="9bfad-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9bfad-136">System.String</span></span>

### <span data-ttu-id="9bfad-137">Microsoft. Azure. Commands. EventHub. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="9bfad-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="9bfad-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bfad-138">OUTPUTS</span></span>

### <span data-ttu-id="9bfad-139">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="9bfad-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="9bfad-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="9bfad-140">NOTES</span></span>

## <span data-ttu-id="9bfad-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9bfad-141">RELATED LINKS</span></span>