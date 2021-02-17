---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: bc869f6bccd2b87927b0cbe3b73cedc1999a261c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236516"
---
# <span data-ttu-id="608b8-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="608b8-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="608b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="608b8-102">SYNOPSIS</span></span>
<span data-ttu-id="608b8-103">Обновляет политику брандмауэра шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="608b8-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="608b8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="608b8-104">SYNTAX</span></span>

### <span data-ttu-id="608b8-105">ByFactoryObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="608b8-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="608b8-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="608b8-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="608b8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="608b8-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="608b8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="608b8-108">DESCRIPTION</span></span>
<span data-ttu-id="608b8-109">**Cmdlet Set-AzApplicationGatewayFirewallPolicy** обновляет политику брандмауэра шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="608b8-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="608b8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="608b8-110">EXAMPLES</span></span>

### <span data-ttu-id="608b8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="608b8-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="608b8-112">Эта команда обновляет политику брандмауэра шлюза приложения с параметрами в переменной $AppGwFirewallPolicy и сохраняет обновленный шлюз в $UpdatedAppGwFirewallPolicy переменной.</span><span class="sxs-lookup"><span data-stu-id="608b8-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="608b8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="608b8-113">PARAMETERS</span></span>

### <span data-ttu-id="608b8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="608b8-114">-AsJob</span></span>
<span data-ttu-id="608b8-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="608b8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="608b8-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="608b8-116">-CustomRule</span></span>
<span data-ttu-id="608b8-117">Список customRules</span><span class="sxs-lookup"><span data-stu-id="608b8-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="608b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="608b8-118">-DefaultProfile</span></span>
<span data-ttu-id="608b8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="608b8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="608b8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="608b8-120">-InputObject</span></span>
<span data-ttu-id="608b8-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="608b8-121">The applicationGatewayFirewallPolicy</span></span>

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

### <span data-ttu-id="608b8-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="608b8-122">-ManagedRule</span></span>
<span data-ttu-id="608b8-123">ManagedRules политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="608b8-123">ManagedRules of the firewall policy</span></span>

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

### <span data-ttu-id="608b8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="608b8-124">-Name</span></span>
<span data-ttu-id="608b8-125">Имя политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="608b8-125">The Firewall Policy Name.</span></span>

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

### <span data-ttu-id="608b8-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="608b8-126">-PolicySetting</span></span>
<span data-ttu-id="608b8-127">Политика настройки политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="608b8-127">Policysettings of the firewall policy</span></span>

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

### <span data-ttu-id="608b8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="608b8-128">-ResourceGroupName</span></span>
<span data-ttu-id="608b8-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="608b8-129">The resource group name.</span></span>

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

### <span data-ttu-id="608b8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="608b8-130">-ResourceId</span></span>
<span data-ttu-id="608b8-131">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="608b8-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="608b8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="608b8-132">-Confirm</span></span>
<span data-ttu-id="608b8-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="608b8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="608b8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="608b8-134">-WhatIf</span></span>
<span data-ttu-id="608b8-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="608b8-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="608b8-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="608b8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="608b8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="608b8-137">CommonParameters</span></span>
<span data-ttu-id="608b8-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="608b8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="608b8-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="608b8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="608b8-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="608b8-140">INPUTS</span></span>

### <span data-ttu-id="608b8-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="608b8-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="608b8-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="608b8-142">OUTPUTS</span></span>

### <span data-ttu-id="608b8-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="608b8-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="608b8-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="608b8-144">NOTES</span></span>

## <span data-ttu-id="608b8-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="608b8-145">RELATED LINKS</span></span>
