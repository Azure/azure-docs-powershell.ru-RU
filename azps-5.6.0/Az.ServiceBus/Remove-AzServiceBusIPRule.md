---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
ms.openlocfilehash: e14d82fbf503487ddb4e4ebac1385400305e9209
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003080"
---
# <span data-ttu-id="1c015-101">Remove-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="1c015-101">Remove-AzServiceBusIPRule</span></span>

## <span data-ttu-id="1c015-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c015-102">SYNOPSIS</span></span>
<span data-ttu-id="1c015-103">Удаление одного правила IP-адреса для NetworkRuleSet данного пространства имен</span><span class="sxs-lookup"><span data-stu-id="1c015-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="1c015-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1c015-104">SYNTAX</span></span>

### <span data-ttu-id="1c015-105">IPRulePropertiesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1c015-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c015-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c015-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c015-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c015-107">DESCRIPTION</span></span>
<span data-ttu-id="1c015-108">Удаление одного правила IP-адреса для NetworkRuleSet данного пространства имен</span><span class="sxs-lookup"><span data-stu-id="1c015-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="1c015-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1c015-109">EXAMPLES</span></span>

### <span data-ttu-id="1c015-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1c015-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="1c015-111">Удаляет IpMask из NetworkRuleSet заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1c015-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="1c015-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c015-112">PARAMETERS</span></span>

### <span data-ttu-id="1c015-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c015-113">-AsJob</span></span>
<span data-ttu-id="1c015-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1c015-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c015-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c015-115">-DefaultProfile</span></span>
<span data-ttu-id="1c015-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c015-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c015-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="1c015-117">-IpMask</span></span>
<span data-ttu-id="1c015-118">ИД ресурсов подсети</span><span class="sxs-lookup"><span data-stu-id="1c015-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="1c015-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="1c015-119">-IpRuleObject</span></span>
<span data-ttu-id="1c015-120">Объект конфигурации IPRule</span><span class="sxs-lookup"><span data-stu-id="1c015-120">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="1c015-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1c015-121">-Name</span></span>
<span data-ttu-id="1c015-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="1c015-122">Namespace Name</span></span>

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

### <span data-ttu-id="1c015-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c015-123">-PassThru</span></span>
<span data-ttu-id="1c015-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1c015-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1c015-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c015-125">-ResourceGroupName</span></span>
<span data-ttu-id="1c015-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1c015-126">Resource Group Name</span></span>

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

### <span data-ttu-id="1c015-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c015-127">-Confirm</span></span>
<span data-ttu-id="1c015-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c015-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c015-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c015-129">-WhatIf</span></span>
<span data-ttu-id="1c015-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c015-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c015-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1c015-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c015-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c015-132">CommonParameters</span></span>
<span data-ttu-id="1c015-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c015-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1c015-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c015-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c015-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c015-135">INPUTS</span></span>

### <span data-ttu-id="1c015-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1c015-136">System.String</span></span>

### <span data-ttu-id="1c015-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="1c015-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="1c015-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1c015-138">OUTPUTS</span></span>

### <span data-ttu-id="1c015-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="1c015-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="1c015-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1c015-140">NOTES</span></span>

## <span data-ttu-id="1c015-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c015-141">RELATED LINKS</span></span>
