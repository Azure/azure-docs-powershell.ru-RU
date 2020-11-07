---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 75c8f7b52fec0e429820d43f86a8a41798b1d5f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902102"
---
# <span data-ttu-id="8e510-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8e510-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="8e510-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e510-102">SYNOPSIS</span></span>
<span data-ttu-id="8e510-103">Создание службы частной ссылки</span><span class="sxs-lookup"><span data-stu-id="8e510-103">Creates a private link service</span></span>

## <span data-ttu-id="8e510-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e510-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e510-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e510-105">DESCRIPTION</span></span>
<span data-ttu-id="8e510-106">Командлет **New-AzPrivateLinkService** создает службу частной ссылки</span><span class="sxs-lookup"><span data-stu-id="8e510-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="8e510-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e510-107">EXAMPLES</span></span>

### <span data-ttu-id="8e510-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8e510-108">Example 1</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
New-AzPrivateLinkService -Name "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

<span data-ttu-id="8e510-109">В этом примере создается служба частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="8e510-109">This example creates a private link service.</span></span>

## <span data-ttu-id="8e510-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e510-110">PARAMETERS</span></span>

### <span data-ttu-id="8e510-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e510-111">-AsJob</span></span>
<span data-ttu-id="8e510-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8e510-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e510-113">-Автоматическое утверждение</span><span class="sxs-lookup"><span data-stu-id="8e510-113">-AutoApproval</span></span>
<span data-ttu-id="8e510-114">Подписка на автоматическое утверждение службы частной ссылки</span><span class="sxs-lookup"><span data-stu-id="8e510-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="8e510-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e510-115">-DefaultProfile</span></span>
<span data-ttu-id="8e510-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e510-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e510-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8e510-117">-Force</span></span>
<span data-ttu-id="8e510-118">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="8e510-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8e510-119">-Конфигурацию</span><span class="sxs-lookup"><span data-stu-id="8e510-119">-IpConfiguration</span></span>
<span data-ttu-id="8e510-120">Конфигурации IP</span><span class="sxs-lookup"><span data-stu-id="8e510-120">The ip configurations</span></span>

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

### <span data-ttu-id="8e510-121">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e510-121">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="8e510-122">IP-конфигурации переднего плана</span><span class="sxs-lookup"><span data-stu-id="8e510-122">The front end ip configurations</span></span>

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

### <span data-ttu-id="8e510-123">-Location</span><span class="sxs-lookup"><span data-stu-id="8e510-123">-Location</span></span>
<span data-ttu-id="8e510-124">поиска.</span><span class="sxs-lookup"><span data-stu-id="8e510-124">location.</span></span>

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

### <span data-ttu-id="8e510-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8e510-125">-Name</span></span>
<span data-ttu-id="8e510-126">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="8e510-126">The name of the service.</span></span>

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

### <span data-ttu-id="8e510-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e510-127">-ResourceGroupName</span></span>
<span data-ttu-id="8e510-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e510-128">The resource group name.</span></span>

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

### <span data-ttu-id="8e510-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="8e510-129">-Tag</span></span>
<span data-ttu-id="8e510-130">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="8e510-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8e510-131">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="8e510-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8e510-132">-Visibility</span><span class="sxs-lookup"><span data-stu-id="8e510-132">-Visibility</span></span>
<span data-ttu-id="8e510-133">Подписка на доступность службы частной ссылки</span><span class="sxs-lookup"><span data-stu-id="8e510-133">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="8e510-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e510-134">-Confirm</span></span>
<span data-ttu-id="8e510-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8e510-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e510-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e510-136">-WhatIf</span></span>
<span data-ttu-id="8e510-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8e510-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e510-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8e510-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e510-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e510-139">CommonParameters</span></span>
<span data-ttu-id="8e510-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e510-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e510-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e510-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e510-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e510-142">INPUTS</span></span>

### <span data-ttu-id="8e510-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8e510-143">System.String</span></span>

### <span data-ttu-id="8e510-144">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="8e510-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="8e510-145">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="8e510-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="8e510-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e510-146">OUTPUTS</span></span>

### <span data-ttu-id="8e510-147">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8e510-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="8e510-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e510-148">NOTES</span></span>

## <span data-ttu-id="8e510-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e510-149">RELATED LINKS</span></span>

[<span data-ttu-id="8e510-150">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8e510-150">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="8e510-151">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8e510-151">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="8e510-152">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8e510-152">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
