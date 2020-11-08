---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 0b4cc79358723e6249a0c9d4e22929e224165402
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073263"
---
# <span data-ttu-id="db822-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="db822-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="db822-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db822-102">SYNOPSIS</span></span>
<span data-ttu-id="db822-103">Создание службы частной ссылки</span><span class="sxs-lookup"><span data-stu-id="db822-103">Creates a private link service</span></span>

## <span data-ttu-id="db822-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db822-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db822-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db822-105">DESCRIPTION</span></span>
<span data-ttu-id="db822-106">Командлет **New-AzPrivateLinkService** создает службу частной ссылки</span><span class="sxs-lookup"><span data-stu-id="db822-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="db822-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db822-107">EXAMPLES</span></span>

### <span data-ttu-id="db822-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="db822-108">Example 1</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
New-AzPrivateLinkService -Name "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

<span data-ttu-id="db822-109">В этом примере создается служба частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="db822-109">This example creates a private link service.</span></span>

## <span data-ttu-id="db822-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db822-110">PARAMETERS</span></span>

### <span data-ttu-id="db822-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db822-111">-AsJob</span></span>
<span data-ttu-id="db822-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="db822-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db822-113">-Автоматическое утверждение</span><span class="sxs-lookup"><span data-stu-id="db822-113">-AutoApproval</span></span>
<span data-ttu-id="db822-114">Подписка на автоматическое утверждение службы частной ссылки</span><span class="sxs-lookup"><span data-stu-id="db822-114">The auto approval subscriptions of private link service</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db822-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db822-115">-DefaultProfile</span></span>
<span data-ttu-id="db822-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db822-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db822-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="db822-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="db822-118">Включите протокол прокси для службы частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="db822-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="db822-119">-Force</span><span class="sxs-lookup"><span data-stu-id="db822-119">-Force</span></span>
<span data-ttu-id="db822-120">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="db822-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="db822-121">-Конфигурацию</span><span class="sxs-lookup"><span data-stu-id="db822-121">-IpConfiguration</span></span>
<span data-ttu-id="db822-122">Конфигурации IP</span><span class="sxs-lookup"><span data-stu-id="db822-122">The ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db822-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="db822-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="db822-124">IP-конфигурации переднего плана</span><span class="sxs-lookup"><span data-stu-id="db822-124">The front end ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db822-125">-Location</span><span class="sxs-lookup"><span data-stu-id="db822-125">-Location</span></span>
<span data-ttu-id="db822-126">поиска.</span><span class="sxs-lookup"><span data-stu-id="db822-126">location.</span></span>

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

### <span data-ttu-id="db822-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="db822-127">-Name</span></span>
<span data-ttu-id="db822-128">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="db822-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db822-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db822-129">-ResourceGroupName</span></span>
<span data-ttu-id="db822-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="db822-130">The resource group name.</span></span>

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

### <span data-ttu-id="db822-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="db822-131">-Tag</span></span>
<span data-ttu-id="db822-132">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="db822-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="db822-133">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="db822-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="db822-134">-Visibility</span><span class="sxs-lookup"><span data-stu-id="db822-134">-Visibility</span></span>
<span data-ttu-id="db822-135">Подписка на доступность службы частной ссылки</span><span class="sxs-lookup"><span data-stu-id="db822-135">The visibility subscriptions of private link service</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db822-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db822-136">-Confirm</span></span>
<span data-ttu-id="db822-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="db822-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db822-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db822-138">-WhatIf</span></span>
<span data-ttu-id="db822-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="db822-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db822-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="db822-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db822-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db822-141">CommonParameters</span></span>
<span data-ttu-id="db822-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db822-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db822-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db822-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db822-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db822-144">INPUTS</span></span>

### <span data-ttu-id="db822-145">System. String</span><span class="sxs-lookup"><span data-stu-id="db822-145">System.String</span></span>

### <span data-ttu-id="db822-146">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="db822-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="db822-147">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="db822-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="db822-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db822-148">OUTPUTS</span></span>

### <span data-ttu-id="db822-149">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="db822-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="db822-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="db822-150">NOTES</span></span>

## <span data-ttu-id="db822-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db822-151">RELATED LINKS</span></span>

[<span data-ttu-id="db822-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="db822-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="db822-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="db822-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="db822-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="db822-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
