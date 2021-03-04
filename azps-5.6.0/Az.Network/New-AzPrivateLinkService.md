---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 9ed82247ff0b1813293059a7608557184bdb18ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958259"
---
# <span data-ttu-id="18597-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="18597-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="18597-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18597-102">SYNOPSIS</span></span>
<span data-ttu-id="18597-103">Создание закрытой службы ссылок</span><span class="sxs-lookup"><span data-stu-id="18597-103">Creates a private link service</span></span>

## <span data-ttu-id="18597-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="18597-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18597-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18597-105">DESCRIPTION</span></span>
<span data-ttu-id="18597-106">Для создания закрытой службы ссылок создается личная служба **AzPrivateLinkService.**</span><span class="sxs-lookup"><span data-stu-id="18597-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="18597-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="18597-107">EXAMPLES</span></span>

### <span data-ttu-id="18597-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="18597-108">Example 1</span></span>

<span data-ttu-id="18597-109">В следующем примере создается частная служба ссылок.</span><span class="sxs-lookup"><span data-stu-id="18597-109">The following example creates a private link service.</span></span>

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

## <span data-ttu-id="18597-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18597-110">PARAMETERS</span></span>

### <span data-ttu-id="18597-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18597-111">-AsJob</span></span>
<span data-ttu-id="18597-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="18597-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18597-113">-AutoApproval</span><span class="sxs-lookup"><span data-stu-id="18597-113">-AutoApproval</span></span>
<span data-ttu-id="18597-114">Подписки на автоматическое утверждение для службы частных ссылок</span><span class="sxs-lookup"><span data-stu-id="18597-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="18597-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18597-115">-DefaultProfile</span></span>
<span data-ttu-id="18597-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18597-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18597-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="18597-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="18597-118">Включить прокси-протокол для службы частных ссылок.</span><span class="sxs-lookup"><span data-stu-id="18597-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="18597-119">-Force</span><span class="sxs-lookup"><span data-stu-id="18597-119">-Force</span></span>
<span data-ttu-id="18597-120">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="18597-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="18597-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="18597-121">-IpConfiguration</span></span>
<span data-ttu-id="18597-122">Конфигурации IP-адресов</span><span class="sxs-lookup"><span data-stu-id="18597-122">The ip configurations</span></span>

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

### <span data-ttu-id="18597-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="18597-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="18597-124">Конфигурация переднего ip-адреса</span><span class="sxs-lookup"><span data-stu-id="18597-124">The front end ip configurations</span></span>

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

### <span data-ttu-id="18597-125">-Location</span><span class="sxs-lookup"><span data-stu-id="18597-125">-Location</span></span>
<span data-ttu-id="18597-126">расположение.</span><span class="sxs-lookup"><span data-stu-id="18597-126">location.</span></span>

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

### <span data-ttu-id="18597-127">-Name</span><span class="sxs-lookup"><span data-stu-id="18597-127">-Name</span></span>
<span data-ttu-id="18597-128">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="18597-128">The name of the service.</span></span>

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

### <span data-ttu-id="18597-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18597-129">-ResourceGroupName</span></span>
<span data-ttu-id="18597-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="18597-130">The resource group name.</span></span>

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

### <span data-ttu-id="18597-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="18597-131">-Tag</span></span>
<span data-ttu-id="18597-132">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="18597-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="18597-133">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="18597-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="18597-134">-Видимость</span><span class="sxs-lookup"><span data-stu-id="18597-134">-Visibility</span></span>
<span data-ttu-id="18597-135">Подписки видимости для службы частных ссылок</span><span class="sxs-lookup"><span data-stu-id="18597-135">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="18597-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18597-136">-Confirm</span></span>
<span data-ttu-id="18597-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="18597-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18597-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18597-138">-WhatIf</span></span>
<span data-ttu-id="18597-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18597-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18597-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="18597-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18597-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18597-141">CommonParameters</span></span>
<span data-ttu-id="18597-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18597-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18597-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18597-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18597-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18597-144">INPUTS</span></span>

### <span data-ttu-id="18597-145">System.String</span><span class="sxs-lookup"><span data-stu-id="18597-145">System.String</span></span>

### <span data-ttu-id="18597-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="18597-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="18597-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="18597-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="18597-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="18597-148">OUTPUTS</span></span>

### <span data-ttu-id="18597-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="18597-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="18597-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="18597-150">NOTES</span></span>

## <span data-ttu-id="18597-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18597-151">RELATED LINKS</span></span>

[<span data-ttu-id="18597-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="18597-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="18597-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="18597-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="18597-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="18597-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
