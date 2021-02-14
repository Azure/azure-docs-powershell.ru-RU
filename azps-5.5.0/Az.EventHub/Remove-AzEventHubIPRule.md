---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
ms.openlocfilehash: 00213d4829d4b389f19a01ad9748517608657136
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237846"
---
# <span data-ttu-id="4ed78-101">Remove-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="4ed78-101">Remove-AzEventHubIPRule</span></span>

## <span data-ttu-id="4ed78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ed78-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed78-103">Удаление одного правила IP-адреса для NetworkRuleSet данного пространства имен</span><span class="sxs-lookup"><span data-stu-id="4ed78-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="4ed78-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4ed78-104">SYNTAX</span></span>

### <span data-ttu-id="4ed78-105">IPRulePropertiesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ed78-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ed78-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ed78-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ed78-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ed78-107">DESCRIPTION</span></span>
<span data-ttu-id="4ed78-108">Удаление одного правила IP-адреса для NetworkRuleSet данного пространства имен</span><span class="sxs-lookup"><span data-stu-id="4ed78-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="4ed78-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4ed78-109">EXAMPLES</span></span>

### <span data-ttu-id="4ed78-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4ed78-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="4ed78-111">Удаляет IpMask из NetworkRuleSet заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="4ed78-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="4ed78-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ed78-112">PARAMETERS</span></span>

### <span data-ttu-id="4ed78-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ed78-113">-AsJob</span></span>
<span data-ttu-id="4ed78-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4ed78-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ed78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed78-115">-DefaultProfile</span></span>
<span data-ttu-id="4ed78-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ed78-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ed78-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="4ed78-117">-IpMask</span></span>
<span data-ttu-id="4ed78-118">ИД ресурса подсети</span><span class="sxs-lookup"><span data-stu-id="4ed78-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="4ed78-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="4ed78-119">-IpRuleObject</span></span>
<span data-ttu-id="4ed78-120">Объект конфигурации IPRule</span><span class="sxs-lookup"><span data-stu-id="4ed78-120">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="4ed78-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4ed78-121">-Name</span></span>
<span data-ttu-id="4ed78-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="4ed78-122">Namespace Name</span></span>

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

### <span data-ttu-id="4ed78-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ed78-123">-PassThru</span></span>
<span data-ttu-id="4ed78-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4ed78-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4ed78-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ed78-125">-ResourceGroupName</span></span>
<span data-ttu-id="4ed78-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4ed78-126">Resource Group Name</span></span>

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

### <span data-ttu-id="4ed78-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ed78-127">-Confirm</span></span>
<span data-ttu-id="4ed78-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ed78-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ed78-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ed78-129">-WhatIf</span></span>
<span data-ttu-id="4ed78-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ed78-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ed78-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4ed78-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ed78-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed78-132">CommonParameters</span></span>
<span data-ttu-id="4ed78-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ed78-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4ed78-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ed78-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed78-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ed78-135">INPUTS</span></span>

### <span data-ttu-id="4ed78-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4ed78-136">System.String</span></span>

### <span data-ttu-id="4ed78-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="4ed78-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="4ed78-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4ed78-138">OUTPUTS</span></span>

### <span data-ttu-id="4ed78-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="4ed78-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="4ed78-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4ed78-140">NOTES</span></span>

## <span data-ttu-id="4ed78-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ed78-141">RELATED LINKS</span></span>