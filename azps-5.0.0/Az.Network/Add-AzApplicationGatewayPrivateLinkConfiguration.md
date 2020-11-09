---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2083dd00c5163a67492ff9973fdf7399d67d7cb6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246573"
---
# <span data-ttu-id="c0fde-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0fde-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="c0fde-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0fde-102">SYNOPSIS</span></span>
<span data-ttu-id="c0fde-103">Добавляет конфигурацию частной ссылки в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="c0fde-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="c0fde-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0fde-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0fde-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0fde-105">DESCRIPTION</span></span>
<span data-ttu-id="c0fde-106">Командлет **Add-AzApplicationGatewayPrivateLinkConfiguration** добавляет конфигурацию частной ссылки в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="c0fde-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="c0fde-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0fde-107">EXAMPLES</span></span>

### <span data-ttu-id="c0fde-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c0fde-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="c0fde-109">Первая команда создает объект privateLinkIpConfiguration и сохраняет его в переменной $PrivateLinkIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c0fde-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="c0fde-110">Вторая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c0fde-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c0fde-111">Третья команда добавляет конфигурацию частной ссылки с именем privateLinkConfig01 для шлюза в $AppGw</span><span class="sxs-lookup"><span data-stu-id="c0fde-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="c0fde-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0fde-112">PARAMETERS</span></span>

### <span data-ttu-id="c0fde-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0fde-113">-ApplicationGateway</span></span>
<span data-ttu-id="c0fde-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0fde-114">The applicationGateway</span></span>

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

### <span data-ttu-id="c0fde-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0fde-115">-DefaultProfile</span></span>
<span data-ttu-id="c0fde-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0fde-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0fde-117">-Конфигурацию</span><span class="sxs-lookup"><span data-stu-id="c0fde-117">-IpConfiguration</span></span>
<span data-ttu-id="c0fde-118">Список IP.</span><span class="sxs-lookup"><span data-stu-id="c0fde-118">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="c0fde-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c0fde-119">-Name</span></span>
<span data-ttu-id="c0fde-120">Имя конфигурации privateLink</span><span class="sxs-lookup"><span data-stu-id="c0fde-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="c0fde-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0fde-121">CommonParameters</span></span>
<span data-ttu-id="c0fde-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0fde-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0fde-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0fde-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0fde-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0fde-124">INPUTS</span></span>

### <span data-ttu-id="c0fde-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0fde-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="c0fde-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="c0fde-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="c0fde-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0fde-127">OUTPUTS</span></span>

### <span data-ttu-id="c0fde-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0fde-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c0fde-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0fde-129">NOTES</span></span>

## <span data-ttu-id="c0fde-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0fde-130">RELATED LINKS</span></span>

[<span data-ttu-id="c0fde-131">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0fde-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="c0fde-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0fde-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="c0fde-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0fde-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="c0fde-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0fde-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)