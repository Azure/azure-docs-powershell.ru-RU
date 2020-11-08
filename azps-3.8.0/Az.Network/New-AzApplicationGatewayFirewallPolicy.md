---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: da83c8cd863d8d3cfa62d47c7a4126d15c4dd670
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074818"
---
# <span data-ttu-id="41a01-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="41a01-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="41a01-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41a01-102">SYNOPSIS</span></span>
<span data-ttu-id="41a01-103">Создание политики брандмауэра для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="41a01-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="41a01-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41a01-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41a01-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41a01-105">DESCRIPTION</span></span>
<span data-ttu-id="41a01-106">Командлет **New-AzApplicationGatewayFirewallPolicy** создает политику брандмауэра для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="41a01-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="41a01-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41a01-107">EXAMPLES</span></span>

### <span data-ttu-id="41a01-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="41a01-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRules $customRule
```

<span data-ttu-id="41a01-109">Эта команда создает новую политику брандмауэра для шлюза приложений Azure с именем "wafResource1" в группе ресурсов "Rg1" в папке "westus" с пользовательскими правилами, определенными в переменной $customRule</span><span class="sxs-lookup"><span data-stu-id="41a01-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="41a01-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41a01-110">PARAMETERS</span></span>

### <span data-ttu-id="41a01-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41a01-111">-AsJob</span></span>
<span data-ttu-id="41a01-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="41a01-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41a01-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="41a01-113">-CustomRule</span></span>
<span data-ttu-id="41a01-114">Список CustomRules</span><span class="sxs-lookup"><span data-stu-id="41a01-114">The list of CustomRules</span></span>

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

### <span data-ttu-id="41a01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41a01-115">-DefaultProfile</span></span>
<span data-ttu-id="41a01-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41a01-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41a01-117">-Force</span><span class="sxs-lookup"><span data-stu-id="41a01-117">-Force</span></span>
<span data-ttu-id="41a01-118">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="41a01-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="41a01-119">-Location</span><span class="sxs-lookup"><span data-stu-id="41a01-119">-Location</span></span>
<span data-ttu-id="41a01-120">поиска.</span><span class="sxs-lookup"><span data-stu-id="41a01-120">location.</span></span>

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

### <span data-ttu-id="41a01-121">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="41a01-121">-ManagedRule</span></span>
<span data-ttu-id="41a01-122">Параметр управляемого правила</span><span class="sxs-lookup"><span data-stu-id="41a01-122">Managed Rule Setting</span></span>

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

### <span data-ttu-id="41a01-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="41a01-123">-Name</span></span>
<span data-ttu-id="41a01-124">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="41a01-124">The resource name.</span></span>

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

### <span data-ttu-id="41a01-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="41a01-125">-PolicySetting</span></span>
<span data-ttu-id="41a01-126">Параметры политики для брандмауэра веб-приложения</span><span class="sxs-lookup"><span data-stu-id="41a01-126">Policy Settings for Web Application Firewall</span></span>

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

### <span data-ttu-id="41a01-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41a01-127">-ResourceGroupName</span></span>
<span data-ttu-id="41a01-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41a01-128">The resource group name.</span></span>

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

### <span data-ttu-id="41a01-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="41a01-129">-Tag</span></span>
<span data-ttu-id="41a01-130">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41a01-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="41a01-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41a01-131">-Confirm</span></span>
<span data-ttu-id="41a01-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="41a01-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41a01-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41a01-133">-WhatIf</span></span>
<span data-ttu-id="41a01-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="41a01-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41a01-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="41a01-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41a01-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41a01-136">CommonParameters</span></span>
<span data-ttu-id="41a01-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41a01-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41a01-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41a01-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41a01-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41a01-139">INPUTS</span></span>

### <span data-ttu-id="41a01-140">System. String</span><span class="sxs-lookup"><span data-stu-id="41a01-140">System.String</span></span>

### <span data-ttu-id="41a01-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallCustomRule []</span><span class="sxs-lookup"><span data-stu-id="41a01-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="41a01-142">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="41a01-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="41a01-143">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="41a01-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="41a01-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="41a01-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="41a01-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41a01-145">OUTPUTS</span></span>

### <span data-ttu-id="41a01-146">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="41a01-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="41a01-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="41a01-147">NOTES</span></span>

## <span data-ttu-id="41a01-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41a01-148">RELATED LINKS</span></span>
