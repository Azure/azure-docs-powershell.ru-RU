---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 78af871cf476ee80c57e22e2469b48bb4d4337a1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421447"
---
# <span data-ttu-id="d67e2-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d67e2-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="d67e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d67e2-102">SYNOPSIS</span></span>
<span data-ttu-id="d67e2-103">Изменяет конфигурацию PrivateLink для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="d67e2-103">Modifies an PrivateLink Configuration for an application gateway.</span></span>

## <span data-ttu-id="d67e2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d67e2-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d67e2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d67e2-105">DESCRIPTION</span></span>
<span data-ttu-id="d67e2-106">**Cmdlet Set-AzApplicationGatewayPrivateLinkConfiguration** изменяет конфигурацию PrivateLink для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="d67e2-106">The **Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet modifies an privateLink configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="d67e2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d67e2-107">EXAMPLES</span></span>

### <span data-ttu-id="d67e2-108">Пример 1. Настройка конфигурации PrivateLink</span><span class="sxs-lookup"><span data-stu-id="d67e2-108">Example 1: Set a PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration01
```

<span data-ttu-id="d67e2-109">Первая команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="d67e2-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d67e2-110">Вторая команда задает конфигурацию PrivateLink с именем privateLinkConfig01, чтобы использовать конфигурацию IP-адреса, храняную в $privateLinkIpConfiguration 01</span><span class="sxs-lookup"><span data-stu-id="d67e2-110">The second command sets the privateLink configuration with name privateLinkConfig01 to use the ip configuration stored in $privateLinkIpConfiguration01</span></span>

## <span data-ttu-id="d67e2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d67e2-111">PARAMETERS</span></span>

### <span data-ttu-id="d67e2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d67e2-112">-ApplicationGateway</span></span>
<span data-ttu-id="d67e2-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d67e2-113">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d67e2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d67e2-114">-DefaultProfile</span></span>
<span data-ttu-id="d67e2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d67e2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d67e2-116">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d67e2-116">-IpConfiguration</span></span>
<span data-ttu-id="d67e2-117">Список ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="d67e2-117">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d67e2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d67e2-118">-Name</span></span>
<span data-ttu-id="d67e2-119">Имя конфигурации PrivateLink</span><span class="sxs-lookup"><span data-stu-id="d67e2-119">The name of the privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d67e2-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d67e2-120">-Confirm</span></span>
<span data-ttu-id="d67e2-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d67e2-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d67e2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d67e2-122">-WhatIf</span></span>
<span data-ttu-id="d67e2-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d67e2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d67e2-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d67e2-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d67e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d67e2-125">CommonParameters</span></span>
<span data-ttu-id="d67e2-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d67e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d67e2-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d67e2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d67e2-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d67e2-128">INPUTS</span></span>

### <span data-ttu-id="d67e2-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d67e2-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="d67e2-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="d67e2-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="d67e2-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d67e2-131">OUTPUTS</span></span>

### <span data-ttu-id="d67e2-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d67e2-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d67e2-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d67e2-133">NOTES</span></span>

## <span data-ttu-id="d67e2-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d67e2-134">RELATED LINKS</span></span>

[<span data-ttu-id="d67e2-135">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d67e2-135">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="d67e2-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d67e2-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="d67e2-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d67e2-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="d67e2-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d67e2-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)