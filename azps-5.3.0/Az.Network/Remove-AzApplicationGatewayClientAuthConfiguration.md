---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 92d3945e92dc4996fbbe3fc0abbcc296ab141621
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421527"
---
# <span data-ttu-id="c8a36-101">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8a36-101">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="c8a36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8a36-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a36-103">Удаляет конфигурацию проверки подлинности клиента для объекта профиля SSL.</span><span class="sxs-lookup"><span data-stu-id="c8a36-103">Removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="c8a36-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c8a36-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8a36-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8a36-105">DESCRIPTION</span></span>
<span data-ttu-id="c8a36-106">**Cmdlet Remove-AzApplicationGateWayClientAuthConfiguration** удаляет конфигурацию проверки подлинности клиента для объекта профиля SSL.</span><span class="sxs-lookup"><span data-stu-id="c8a36-106">The **Remove-AzApplicationGatewayClientAuthConfiguration** cmdlet removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="c8a36-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c8a36-107">EXAMPLES</span></span>

### <span data-ttu-id="c8a36-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c8a36-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile
```

<span data-ttu-id="c8a36-109">Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="c8a36-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="c8a36-110">Вторая команда получает профиль SSL profile01 для $AppGw и сохраняет его в переменной $profile.</span><span class="sxs-lookup"><span data-stu-id="c8a36-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="c8a36-111">Последняя команда удаляет конфигурацию проверки подлинности клиента для SSL-профиля, храняшегося в $profile.</span><span class="sxs-lookup"><span data-stu-id="c8a36-111">The last command removes the client authentication configuration of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="c8a36-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8a36-112">PARAMETERS</span></span>

### <span data-ttu-id="c8a36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a36-113">-DefaultProfile</span></span>
<span data-ttu-id="c8a36-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a36-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8a36-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="c8a36-115">-SslProfile</span></span>
<span data-ttu-id="c8a36-116">Профиль SSL</span><span class="sxs-lookup"><span data-stu-id="c8a36-116">The ssl profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a36-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a36-117">CommonParameters</span></span>
<span data-ttu-id="c8a36-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8a36-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a36-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8a36-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a36-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8a36-120">INPUTS</span></span>

### <span data-ttu-id="c8a36-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c8a36-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="c8a36-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c8a36-122">OUTPUTS</span></span>

### <span data-ttu-id="c8a36-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c8a36-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="c8a36-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c8a36-124">NOTES</span></span>

## <span data-ttu-id="c8a36-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8a36-125">RELATED LINKS</span></span>

[<span data-ttu-id="c8a36-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8a36-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="c8a36-127">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8a36-127">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="c8a36-128">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8a36-128">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="c8a36-129">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8a36-129">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)