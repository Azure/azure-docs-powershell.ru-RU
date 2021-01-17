---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 03e03de70f61672d1246ffeb8469efe0c04b3ea4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397967"
---
# <span data-ttu-id="b095b-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b095b-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="b095b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b095b-102">SYNOPSIS</span></span>
<span data-ttu-id="b095b-103">Создает политику брандмауэра шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b095b-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="b095b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b095b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b095b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b095b-105">DESCRIPTION</span></span>
<span data-ttu-id="b095b-106">С **помощью cmdlet New-AzApplicationGatewayFirewallPolicy** создается политика брандмауэра шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b095b-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="b095b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b095b-107">EXAMPLES</span></span>

### <span data-ttu-id="b095b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b095b-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRule $customRule
```

<span data-ttu-id="b095b-109">Эта команда создает новую политику брандмауэра шлюза приложения Azure с именем wafResource1 в группе ресурсов "rg1" в расположении "westus" с настраиваемой политикой, заданной в переменной $customRule.</span><span class="sxs-lookup"><span data-stu-id="b095b-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="b095b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b095b-110">PARAMETERS</span></span>

### <span data-ttu-id="b095b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b095b-111">-AsJob</span></span>
<span data-ttu-id="b095b-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b095b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b095b-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="b095b-113">-CustomRule</span></span>
<span data-ttu-id="b095b-114">Список customRules</span><span class="sxs-lookup"><span data-stu-id="b095b-114">The list of CustomRules</span></span>

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

### <span data-ttu-id="b095b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b095b-115">-DefaultProfile</span></span>
<span data-ttu-id="b095b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b095b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b095b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b095b-117">-Force</span></span>
<span data-ttu-id="b095b-118">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="b095b-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b095b-119">-Location</span><span class="sxs-lookup"><span data-stu-id="b095b-119">-Location</span></span>
<span data-ttu-id="b095b-120">расположение.</span><span class="sxs-lookup"><span data-stu-id="b095b-120">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b095b-121">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="b095b-121">-ManagedRule</span></span>
<span data-ttu-id="b095b-122">Параметр управляемого правила</span><span class="sxs-lookup"><span data-stu-id="b095b-122">Managed Rule Setting</span></span>

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

### <span data-ttu-id="b095b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b095b-123">-Name</span></span>
<span data-ttu-id="b095b-124">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="b095b-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b095b-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="b095b-125">-PolicySetting</span></span>
<span data-ttu-id="b095b-126">Параметры политики для брандмауэра веб-приложения</span><span class="sxs-lookup"><span data-stu-id="b095b-126">Policy Settings for Web Application Firewall</span></span>

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

### <span data-ttu-id="b095b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b095b-127">-ResourceGroupName</span></span>
<span data-ttu-id="b095b-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b095b-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b095b-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="b095b-129">-Tag</span></span>
<span data-ttu-id="b095b-130">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="b095b-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b095b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b095b-131">-Confirm</span></span>
<span data-ttu-id="b095b-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b095b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b095b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b095b-133">-WhatIf</span></span>
<span data-ttu-id="b095b-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b095b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b095b-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b095b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b095b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b095b-136">CommonParameters</span></span>
<span data-ttu-id="b095b-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b095b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b095b-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b095b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b095b-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b095b-139">INPUTS</span></span>

### <span data-ttu-id="b095b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b095b-140">System.String</span></span>

### <span data-ttu-id="b095b-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span><span class="sxs-lookup"><span data-stu-id="b095b-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="b095b-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="b095b-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="b095b-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="b095b-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="b095b-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b095b-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b095b-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b095b-145">OUTPUTS</span></span>

### <span data-ttu-id="b095b-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b095b-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="b095b-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b095b-147">NOTES</span></span>

## <span data-ttu-id="b095b-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b095b-148">RELATED LINKS</span></span>
