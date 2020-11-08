---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 2723ca0f5bebfbf65fefbfbd94fa995d544d9f71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248828"
---
# <span data-ttu-id="14eaa-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="14eaa-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="14eaa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="14eaa-103">Создание службы частной ссылки</span><span class="sxs-lookup"><span data-stu-id="14eaa-103">Creates a private link service</span></span>

## <span data-ttu-id="14eaa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14eaa-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14eaa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14eaa-105">DESCRIPTION</span></span>
<span data-ttu-id="14eaa-106">Командлет **New-AzPrivateLinkService** создает службу частной ссылки</span><span class="sxs-lookup"><span data-stu-id="14eaa-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="14eaa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14eaa-107">EXAMPLES</span></span>

### <span data-ttu-id="14eaa-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="14eaa-108">Example 1</span></span>

<span data-ttu-id="14eaa-109">В следующем примере создается служба частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="14eaa-109">The following example creates a private link service.</span></span>

```powershell
$vnet = Get-AzVirtualNetwork -ResourceName 'myvnet' -ResourceGroupName 'myresourcegroup'
# View the results of $vnet and change 'mysubnet' in the following line to the appropriate subnet name.
$subnet = $vnet | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mysubnet'
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name 'IP-Config' -Subnet $subnet -PrivateIpAddress '10.0.0.5'
$publicip = Get-AzPublicIpAddress -ResourceGroupName 'myresourcegroup'
$frontend = New-AzLoadBalancerFrontendIpConfig -Name 'FrontendIpConfig01' -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name 'MyLoadBalancer' -ResourceGroupName 'myresourcegroup' -Location 'West US' -FrontendIpConfiguration $frontend
New-AzPrivateLinkService -Name 'mypls' -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

## <span data-ttu-id="14eaa-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14eaa-110">PARAMETERS</span></span>

### <span data-ttu-id="14eaa-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14eaa-111">-AsJob</span></span>
<span data-ttu-id="14eaa-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="14eaa-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14eaa-113">-Автоматическое утверждение</span><span class="sxs-lookup"><span data-stu-id="14eaa-113">-AutoApproval</span></span>
<span data-ttu-id="14eaa-114">Подписка на автоматическое утверждение службы частной ссылки</span><span class="sxs-lookup"><span data-stu-id="14eaa-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="14eaa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14eaa-115">-DefaultProfile</span></span>
<span data-ttu-id="14eaa-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14eaa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14eaa-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="14eaa-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="14eaa-118">Включите протокол прокси для службы частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="14eaa-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="14eaa-119">-Force</span><span class="sxs-lookup"><span data-stu-id="14eaa-119">-Force</span></span>
<span data-ttu-id="14eaa-120">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="14eaa-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="14eaa-121">-Конфигурацию</span><span class="sxs-lookup"><span data-stu-id="14eaa-121">-IpConfiguration</span></span>
<span data-ttu-id="14eaa-122">Конфигурации IP</span><span class="sxs-lookup"><span data-stu-id="14eaa-122">The ip configurations</span></span>

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

### <span data-ttu-id="14eaa-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="14eaa-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="14eaa-124">IP-конфигурации переднего плана</span><span class="sxs-lookup"><span data-stu-id="14eaa-124">The front end ip configurations</span></span>

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

### <span data-ttu-id="14eaa-125">-Location</span><span class="sxs-lookup"><span data-stu-id="14eaa-125">-Location</span></span>
<span data-ttu-id="14eaa-126">поиска.</span><span class="sxs-lookup"><span data-stu-id="14eaa-126">location.</span></span>

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

### <span data-ttu-id="14eaa-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="14eaa-127">-Name</span></span>
<span data-ttu-id="14eaa-128">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="14eaa-128">The name of the service.</span></span>

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

### <span data-ttu-id="14eaa-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14eaa-129">-ResourceGroupName</span></span>
<span data-ttu-id="14eaa-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="14eaa-130">The resource group name.</span></span>

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

### <span data-ttu-id="14eaa-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="14eaa-131">-Tag</span></span>
<span data-ttu-id="14eaa-132">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="14eaa-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="14eaa-133">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="14eaa-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="14eaa-134">-Visibility</span><span class="sxs-lookup"><span data-stu-id="14eaa-134">-Visibility</span></span>
<span data-ttu-id="14eaa-135">Подписка на доступность службы частной ссылки</span><span class="sxs-lookup"><span data-stu-id="14eaa-135">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="14eaa-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14eaa-136">-Confirm</span></span>
<span data-ttu-id="14eaa-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="14eaa-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14eaa-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14eaa-138">-WhatIf</span></span>
<span data-ttu-id="14eaa-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="14eaa-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14eaa-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="14eaa-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14eaa-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14eaa-141">CommonParameters</span></span>
<span data-ttu-id="14eaa-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14eaa-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14eaa-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14eaa-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14eaa-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14eaa-144">INPUTS</span></span>

### <span data-ttu-id="14eaa-145">System. String</span><span class="sxs-lookup"><span data-stu-id="14eaa-145">System.String</span></span>

### <span data-ttu-id="14eaa-146">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="14eaa-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="14eaa-147">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="14eaa-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="14eaa-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14eaa-148">OUTPUTS</span></span>

### <span data-ttu-id="14eaa-149">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="14eaa-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="14eaa-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="14eaa-150">NOTES</span></span>

## <span data-ttu-id="14eaa-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14eaa-151">RELATED LINKS</span></span>

[<span data-ttu-id="14eaa-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="14eaa-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="14eaa-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="14eaa-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="14eaa-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="14eaa-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
