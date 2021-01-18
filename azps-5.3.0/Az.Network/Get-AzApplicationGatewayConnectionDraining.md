---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b6fe7d8be92e2d82762557a05bf88ef053e0d407
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506528"
---
# <span data-ttu-id="9b15d-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9b15d-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="9b15d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b15d-102">SYNOPSIS</span></span>
<span data-ttu-id="9b15d-103">Получает конфигурацию разрядки подключения для объекта с замещающий http-параметрами.</span><span class="sxs-lookup"><span data-stu-id="9b15d-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="9b15d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9b15d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b15d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b15d-105">DESCRIPTION</span></span>
<span data-ttu-id="9b15d-106">С **помощью cmdlet Get-AzApplicationGatewayConnectionDraining** получает конфигурацию разрядки подключения для объекта параметров HTTP.</span><span class="sxs-lookup"><span data-stu-id="9b15d-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="9b15d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9b15d-107">EXAMPLES</span></span>

### <span data-ttu-id="9b15d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9b15d-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="9b15d-109">Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="9b15d-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9b15d-110">Вторая команда получает back-end HTTP-параметры с именем Settings01 для $AppGw и сохраняет их в $Settings переменной.</span><span class="sxs-lookup"><span data-stu-id="9b15d-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="9b15d-111">Последняя команда получает конфигурацию разрядки подключений из веб-параметров HTTP $Settings и сохраняет ее в переменной $ConnectionDraining подключения.</span><span class="sxs-lookup"><span data-stu-id="9b15d-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="9b15d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b15d-112">PARAMETERS</span></span>

### <span data-ttu-id="9b15d-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9b15d-113">-BackendHttpSettings</span></span>
<span data-ttu-id="9b15d-114">Параметры backend http</span><span class="sxs-lookup"><span data-stu-id="9b15d-114">The backend http settings</span></span>

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

### <span data-ttu-id="9b15d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b15d-115">-DefaultProfile</span></span>
<span data-ttu-id="9b15d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b15d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b15d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b15d-117">CommonParameters</span></span>
<span data-ttu-id="9b15d-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b15d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b15d-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b15d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b15d-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b15d-120">INPUTS</span></span>

### <span data-ttu-id="9b15d-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9b15d-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="9b15d-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9b15d-122">OUTPUTS</span></span>

### <span data-ttu-id="9b15d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9b15d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="9b15d-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9b15d-124">NOTES</span></span>

## <span data-ttu-id="9b15d-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b15d-125">RELATED LINKS</span></span>

[<span data-ttu-id="9b15d-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b15d-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="9b15d-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="9b15d-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="9b15d-128">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9b15d-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="9b15d-129">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9b15d-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="9b15d-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9b15d-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
