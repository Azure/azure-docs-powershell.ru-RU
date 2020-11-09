---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 87f6f441220f1f8ab47fee5356bddca8d02b96c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317000"
---
# <span data-ttu-id="a414f-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a414f-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="a414f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a414f-102">SYNOPSIS</span></span>
<span data-ttu-id="a414f-103">Удаление IP-конфигурации с шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="a414f-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="a414f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a414f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a414f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a414f-105">DESCRIPTION</span></span>
<span data-ttu-id="a414f-106">Командлет **Remove-AzApplicationGatewayIPConfiguration** УДАЛЯЕТ конфигурацию IP из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="a414f-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="a414f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a414f-107">EXAMPLES</span></span>

### <span data-ttu-id="a414f-108">Пример 1: Удаление конфигурации IP из шлюза приложений Azure</span><span class="sxs-lookup"><span data-stu-id="a414f-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="a414f-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a414f-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a414f-110">Вторая команда удаляет IP-конфигурацию с именем Subnet02 из шлюза приложений, хранящегося в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a414f-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="a414f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a414f-111">PARAMETERS</span></span>

### <span data-ttu-id="a414f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a414f-112">-ApplicationGateway</span></span>
<span data-ttu-id="a414f-113">Указывает шлюз приложений, из которого нужно удалить конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="a414f-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a414f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a414f-114">-DefaultProfile</span></span>
<span data-ttu-id="a414f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a414f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a414f-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a414f-116">-Name</span></span>
<span data-ttu-id="a414f-117">Указывает имя удаляемой IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a414f-117">Specifies the name of the IP configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a414f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a414f-118">CommonParameters</span></span>
<span data-ttu-id="a414f-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a414f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a414f-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a414f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a414f-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a414f-121">INPUTS</span></span>

### <span data-ttu-id="a414f-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a414f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a414f-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a414f-123">OUTPUTS</span></span>

### <span data-ttu-id="a414f-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a414f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a414f-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="a414f-125">NOTES</span></span>

## <span data-ttu-id="a414f-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a414f-126">RELATED LINKS</span></span>

[<span data-ttu-id="a414f-127">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a414f-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="a414f-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a414f-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="a414f-129">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a414f-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="a414f-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a414f-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


