---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: ddcec36e8561196b31dd94eb15d99a7e2a92a378
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964083"
---
# <span data-ttu-id="6da87-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="6da87-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="6da87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6da87-102">SYNOPSIS</span></span>
<span data-ttu-id="6da87-103">Удаляет конфигурацию разрядки подключения для объекта с замещающий http-параметрами.</span><span class="sxs-lookup"><span data-stu-id="6da87-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="6da87-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6da87-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6da87-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6da87-105">DESCRIPTION</span></span>
<span data-ttu-id="6da87-106">С **помощью cmdlet Remove-AzApplicationGatewayConnectionDraining** удаляется конфигурация разрядки подключения для объекта параметров HTTP.</span><span class="sxs-lookup"><span data-stu-id="6da87-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="6da87-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6da87-107">EXAMPLES</span></span>

### <span data-ttu-id="6da87-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6da87-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="6da87-109">Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="6da87-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6da87-110">Вторая команда получает back-end HTTP-параметры с именем Settings01 для $AppGw и сохраняет их в $Settings переменной.</span><span class="sxs-lookup"><span data-stu-id="6da87-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="6da87-111">Последняя команда удаляет конфигурацию разрядки подключения для конечных параметров HTTP, хранимых в $Settings.</span><span class="sxs-lookup"><span data-stu-id="6da87-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="6da87-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6da87-112">PARAMETERS</span></span>

### <span data-ttu-id="6da87-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6da87-113">-BackendHttpSettings</span></span>
<span data-ttu-id="6da87-114">Параметры backend http</span><span class="sxs-lookup"><span data-stu-id="6da87-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6da87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6da87-115">-DefaultProfile</span></span>
<span data-ttu-id="6da87-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6da87-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6da87-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6da87-117">CommonParameters</span></span>
<span data-ttu-id="6da87-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6da87-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6da87-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6da87-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6da87-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6da87-120">INPUTS</span></span>

### <span data-ttu-id="6da87-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6da87-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="6da87-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6da87-122">OUTPUTS</span></span>

### <span data-ttu-id="6da87-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6da87-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="6da87-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6da87-124">NOTES</span></span>

## <span data-ttu-id="6da87-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6da87-125">RELATED LINKS</span></span>

[<span data-ttu-id="6da87-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6da87-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="6da87-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="6da87-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="6da87-128">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="6da87-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="6da87-129">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="6da87-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="6da87-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="6da87-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

