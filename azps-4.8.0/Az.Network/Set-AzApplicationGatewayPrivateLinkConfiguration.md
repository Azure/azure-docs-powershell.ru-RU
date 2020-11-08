---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 78af871cf476ee80c57e22e2469b48bb4d4337a1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078855"
---
# <span data-ttu-id="6d6f9-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d6f9-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="6d6f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d6f9-102">SYNOPSIS</span></span>
<span data-ttu-id="6d6f9-103">Изменяет конфигурацию PrivateLink для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-103">Modifies an PrivateLink Configuration for an application gateway.</span></span>

## <span data-ttu-id="6d6f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d6f9-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d6f9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d6f9-105">DESCRIPTION</span></span>
<span data-ttu-id="6d6f9-106">Командлет **Set-AzApplicationGatewayPrivateLinkConfiguration** изменяет конфигурацию privateLink для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-106">The **Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet modifies an privateLink configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="6d6f9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d6f9-107">EXAMPLES</span></span>

### <span data-ttu-id="6d6f9-108">Пример 1: Настройка конфигурации PrivateLink</span><span class="sxs-lookup"><span data-stu-id="6d6f9-108">Example 1: Set a PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration01
```

<span data-ttu-id="6d6f9-109">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6d6f9-110">Вторая команда задает конфигурацию privateLink с именем privateLinkConfig01 для использования IP-конфигурации, хранящейся в $privateLinkIpConfiguration 01.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-110">The second command sets the privateLink configuration with name privateLinkConfig01 to use the ip configuration stored in $privateLinkIpConfiguration01</span></span>

## <span data-ttu-id="6d6f9-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d6f9-111">PARAMETERS</span></span>

### <span data-ttu-id="6d6f9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6d6f9-112">-ApplicationGateway</span></span>
<span data-ttu-id="6d6f9-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6d6f9-113">The applicationGateway</span></span>

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

### <span data-ttu-id="6d6f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d6f9-114">-DefaultProfile</span></span>
<span data-ttu-id="6d6f9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d6f9-116">-Конфигурацию</span><span class="sxs-lookup"><span data-stu-id="6d6f9-116">-IpConfiguration</span></span>
<span data-ttu-id="6d6f9-117">Список IP.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-117">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="6d6f9-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6d6f9-118">-Name</span></span>
<span data-ttu-id="6d6f9-119">Имя конфигурации privateLink</span><span class="sxs-lookup"><span data-stu-id="6d6f9-119">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="6d6f9-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d6f9-120">-Confirm</span></span>
<span data-ttu-id="6d6f9-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d6f9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d6f9-122">-WhatIf</span></span>
<span data-ttu-id="6d6f9-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d6f9-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d6f9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d6f9-125">CommonParameters</span></span>
<span data-ttu-id="6d6f9-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d6f9-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d6f9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d6f9-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d6f9-128">INPUTS</span></span>

### <span data-ttu-id="6d6f9-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6d6f9-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="6d6f9-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="6d6f9-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="6d6f9-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d6f9-131">OUTPUTS</span></span>

### <span data-ttu-id="6d6f9-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6d6f9-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6d6f9-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d6f9-133">NOTES</span></span>

## <span data-ttu-id="6d6f9-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d6f9-134">RELATED LINKS</span></span>

[<span data-ttu-id="6d6f9-135">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d6f9-135">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="6d6f9-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d6f9-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="6d6f9-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d6f9-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="6d6f9-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d6f9-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)