---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 87f6f441220f1f8ab47fee5356bddca8d02b96c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410540"
---
# <span data-ttu-id="331d0-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="331d0-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="331d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="331d0-102">SYNOPSIS</span></span>
<span data-ttu-id="331d0-103">Удаляет конфигурацию IP-адреса из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="331d0-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="331d0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="331d0-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="331d0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="331d0-105">DESCRIPTION</span></span>
<span data-ttu-id="331d0-106">**Cmdlet Remove-AzApplicationGatewayIPConfiguration** удаляет конфигурацию IP-адреса из шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="331d0-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="331d0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="331d0-107">EXAMPLES</span></span>

### <span data-ttu-id="331d0-108">Пример 1. Удаление конфигурации IP-адреса из шлюза приложения Azure</span><span class="sxs-lookup"><span data-stu-id="331d0-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="331d0-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="331d0-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="331d0-110">Вторая команда удаляет конфигурацию IP-адреса "Подсеть02" из шлюза приложения, $AppGw.</span><span class="sxs-lookup"><span data-stu-id="331d0-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="331d0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="331d0-111">PARAMETERS</span></span>

### <span data-ttu-id="331d0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="331d0-112">-ApplicationGateway</span></span>
<span data-ttu-id="331d0-113">Указывает шлюз приложения, из которого необходимо удалить конфигурацию IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="331d0-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="331d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="331d0-114">-DefaultProfile</span></span>
<span data-ttu-id="331d0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="331d0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="331d0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="331d0-116">-Name</span></span>
<span data-ttu-id="331d0-117">Указывает имя удаляемой конфигурации IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="331d0-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="331d0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="331d0-118">CommonParameters</span></span>
<span data-ttu-id="331d0-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="331d0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="331d0-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="331d0-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="331d0-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="331d0-121">INPUTS</span></span>

### <span data-ttu-id="331d0-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="331d0-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="331d0-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="331d0-123">OUTPUTS</span></span>

### <span data-ttu-id="331d0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="331d0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="331d0-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="331d0-125">NOTES</span></span>

## <span data-ttu-id="331d0-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="331d0-126">RELATED LINKS</span></span>

[<span data-ttu-id="331d0-127">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="331d0-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="331d0-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="331d0-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="331d0-129">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="331d0-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="331d0-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="331d0-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


