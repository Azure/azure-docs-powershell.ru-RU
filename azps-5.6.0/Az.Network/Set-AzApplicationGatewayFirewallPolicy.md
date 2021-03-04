---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: e6b9c873110118392e9380418276bfa0f4d938a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981704"
---
# <span data-ttu-id="61dd7-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="61dd7-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="61dd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="61dd7-103">Обновляет политику брандмауэра шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="61dd7-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="61dd7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="61dd7-104">SYNTAX</span></span>

### <span data-ttu-id="61dd7-105">ByFactoryObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61dd7-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61dd7-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="61dd7-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61dd7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="61dd7-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61dd7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61dd7-108">DESCRIPTION</span></span>
<span data-ttu-id="61dd7-109">**Cmdlet Set-AzApplicationGatewayFirewallPolicy** обновляет политику брандмауэра шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="61dd7-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="61dd7-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="61dd7-110">EXAMPLES</span></span>

### <span data-ttu-id="61dd7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="61dd7-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="61dd7-112">Эта команда обновляет политику брандмауэра шлюза приложения с параметрами в переменной $AppGwFirewallPolicy и сохраняет обновленный шлюз в $UpdatedAppGwFirewallPolicy переменной.</span><span class="sxs-lookup"><span data-stu-id="61dd7-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="61dd7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61dd7-113">PARAMETERS</span></span>

### <span data-ttu-id="61dd7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61dd7-114">-AsJob</span></span>
<span data-ttu-id="61dd7-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="61dd7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61dd7-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="61dd7-116">-CustomRule</span></span>
<span data-ttu-id="61dd7-117">Список customRules</span><span class="sxs-lookup"><span data-stu-id="61dd7-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="61dd7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61dd7-118">-DefaultProfile</span></span>
<span data-ttu-id="61dd7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61dd7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61dd7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61dd7-120">-InputObject</span></span>
<span data-ttu-id="61dd7-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="61dd7-121">The applicationGatewayFirewallPolicy</span></span>

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

### <span data-ttu-id="61dd7-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="61dd7-122">-ManagedRule</span></span>
<span data-ttu-id="61dd7-123">ManagedRules политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="61dd7-123">ManagedRules of the firewall policy</span></span>

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

### <span data-ttu-id="61dd7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="61dd7-124">-Name</span></span>
<span data-ttu-id="61dd7-125">Имя политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="61dd7-125">The Firewall Policy Name.</span></span>

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

### <span data-ttu-id="61dd7-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="61dd7-126">-PolicySetting</span></span>
<span data-ttu-id="61dd7-127">Политика настройки политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="61dd7-127">Policysettings of the firewall policy</span></span>

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

### <span data-ttu-id="61dd7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61dd7-128">-ResourceGroupName</span></span>
<span data-ttu-id="61dd7-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61dd7-129">The resource group name.</span></span>

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

### <span data-ttu-id="61dd7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61dd7-130">-ResourceId</span></span>
<span data-ttu-id="61dd7-131">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="61dd7-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="61dd7-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61dd7-132">-Confirm</span></span>
<span data-ttu-id="61dd7-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="61dd7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61dd7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61dd7-134">-WhatIf</span></span>
<span data-ttu-id="61dd7-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61dd7-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61dd7-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="61dd7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61dd7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61dd7-137">CommonParameters</span></span>
<span data-ttu-id="61dd7-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61dd7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61dd7-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61dd7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61dd7-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61dd7-140">INPUTS</span></span>

### <span data-ttu-id="61dd7-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="61dd7-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="61dd7-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="61dd7-142">OUTPUTS</span></span>

### <span data-ttu-id="61dd7-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="61dd7-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="61dd7-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="61dd7-144">NOTES</span></span>

## <span data-ttu-id="61dd7-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61dd7-145">RELATED LINKS</span></span>
