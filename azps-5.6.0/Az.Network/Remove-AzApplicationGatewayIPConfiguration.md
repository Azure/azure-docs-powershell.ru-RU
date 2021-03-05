---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 610fe3f2ba4867dc1145488dfe789dba051b23bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987748"
---
# <span data-ttu-id="2cb60-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2cb60-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="2cb60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cb60-102">SYNOPSIS</span></span>
<span data-ttu-id="2cb60-103">Удаляет конфигурацию IP-адреса из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="2cb60-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="2cb60-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2cb60-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cb60-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cb60-105">DESCRIPTION</span></span>
<span data-ttu-id="2cb60-106">**Cmdlet Remove-AzApplicationGatewayIPConfiguration** удаляет конфигурацию IP-адреса из шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="2cb60-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="2cb60-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2cb60-107">EXAMPLES</span></span>

### <span data-ttu-id="2cb60-108">Пример 1. Удаление конфигурации IP-адреса из шлюза приложения Azure</span><span class="sxs-lookup"><span data-stu-id="2cb60-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="2cb60-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2cb60-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2cb60-110">Вторая команда удаляет конфигурацию IP-адреса "Подсеть02" из шлюза приложения, который хранится в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2cb60-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="2cb60-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cb60-111">PARAMETERS</span></span>

### <span data-ttu-id="2cb60-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2cb60-112">-ApplicationGateway</span></span>
<span data-ttu-id="2cb60-113">Указывает шлюз приложения, из которого необходимо удалить конфигурацию IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2cb60-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="2cb60-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cb60-114">-DefaultProfile</span></span>
<span data-ttu-id="2cb60-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2cb60-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cb60-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2cb60-116">-Name</span></span>
<span data-ttu-id="2cb60-117">Указывает имя удаляемой конфигурации IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2cb60-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="2cb60-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cb60-118">CommonParameters</span></span>
<span data-ttu-id="2cb60-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cb60-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cb60-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cb60-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cb60-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2cb60-121">INPUTS</span></span>

### <span data-ttu-id="2cb60-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2cb60-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2cb60-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2cb60-123">OUTPUTS</span></span>

### <span data-ttu-id="2cb60-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2cb60-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2cb60-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2cb60-125">NOTES</span></span>

## <span data-ttu-id="2cb60-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2cb60-126">RELATED LINKS</span></span>

[<span data-ttu-id="2cb60-127">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2cb60-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2cb60-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2cb60-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2cb60-129">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2cb60-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2cb60-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2cb60-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


