---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: bc869f6bccd2b87927b0cbe3b73cedc1999a261c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078857"
---
# <span data-ttu-id="74449-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="74449-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="74449-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74449-102">SYNOPSIS</span></span>
<span data-ttu-id="74449-103">Обновляет политику брандмауэра для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="74449-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="74449-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74449-104">SYNTAX</span></span>

### <span data-ttu-id="74449-105">ByFactoryObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="74449-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74449-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="74449-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74449-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="74449-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74449-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74449-108">DESCRIPTION</span></span>
<span data-ttu-id="74449-109">Командлет **Set-AzApplicationGatewayFirewallPolicy** обновляет политику брандмауэра для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="74449-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="74449-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74449-110">EXAMPLES</span></span>

### <span data-ttu-id="74449-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="74449-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="74449-112">Эта команда обновляет политику брандмауэра для шлюза приложений с помощью параметров в переменной $AppGwFirewallPolicy и сохраняет обновленный шлюз в переменной $UpdatedAppGwFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="74449-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="74449-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74449-113">PARAMETERS</span></span>

### <span data-ttu-id="74449-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74449-114">-AsJob</span></span>
<span data-ttu-id="74449-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="74449-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74449-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="74449-116">-CustomRule</span></span>
<span data-ttu-id="74449-117">Список CustomRules</span><span class="sxs-lookup"><span data-stu-id="74449-117">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74449-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74449-118">-DefaultProfile</span></span>
<span data-ttu-id="74449-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74449-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74449-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74449-120">-InputObject</span></span>
<span data-ttu-id="74449-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="74449-121">The applicationGatewayFirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74449-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="74449-122">-ManagedRule</span></span>
<span data-ttu-id="74449-123">ManagedRules политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="74449-123">ManagedRules of the firewall policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74449-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="74449-124">-Name</span></span>
<span data-ttu-id="74449-125">Имя политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="74449-125">The Firewall Policy Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74449-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="74449-126">-PolicySetting</span></span>
<span data-ttu-id="74449-127">Policysettings политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="74449-127">Policysettings of the firewall policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74449-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74449-128">-ResourceGroupName</span></span>
<span data-ttu-id="74449-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="74449-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74449-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74449-130">-ResourceId</span></span>
<span data-ttu-id="74449-131">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="74449-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74449-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74449-132">-Confirm</span></span>
<span data-ttu-id="74449-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="74449-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74449-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74449-134">-WhatIf</span></span>
<span data-ttu-id="74449-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="74449-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74449-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="74449-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74449-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74449-137">CommonParameters</span></span>
<span data-ttu-id="74449-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74449-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74449-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74449-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74449-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74449-140">INPUTS</span></span>

### <span data-ttu-id="74449-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="74449-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="74449-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74449-142">OUTPUTS</span></span>

### <span data-ttu-id="74449-143">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="74449-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="74449-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="74449-144">NOTES</span></span>

## <span data-ttu-id="74449-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74449-145">RELATED LINKS</span></span>