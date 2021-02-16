---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: cba24e2da43bce34c42a17c9717ed8c2314a00b1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400116"
---
# <span data-ttu-id="eff9b-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="eff9b-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="eff9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eff9b-102">SYNOPSIS</span></span>
<span data-ttu-id="eff9b-103">Удаляет конфигурацию разрядки подключения для объекта с замещающий http-параметрами.</span><span class="sxs-lookup"><span data-stu-id="eff9b-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="eff9b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eff9b-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eff9b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eff9b-105">DESCRIPTION</span></span>
<span data-ttu-id="eff9b-106">С **помощью cmdlet Remove-AzApplicationGatewayConnectionDraining** удаляется конфигурация разрядки подключения для объекта параметров HTTP.</span><span class="sxs-lookup"><span data-stu-id="eff9b-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="eff9b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eff9b-107">EXAMPLES</span></span>

### <span data-ttu-id="eff9b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eff9b-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="eff9b-109">Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в $AppGw переменной.</span><span class="sxs-lookup"><span data-stu-id="eff9b-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="eff9b-110">Вторая команда получает back-end HTTP-параметры с именем Settings01 для $AppGw и сохраняет их в $Settings переменной.</span><span class="sxs-lookup"><span data-stu-id="eff9b-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="eff9b-111">Последняя команда удаляет конфигурацию разрядки подключения для конечных параметров HTTP, хранимых в $Settings.</span><span class="sxs-lookup"><span data-stu-id="eff9b-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="eff9b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eff9b-112">PARAMETERS</span></span>

### <span data-ttu-id="eff9b-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="eff9b-113">-BackendHttpSettings</span></span>
<span data-ttu-id="eff9b-114">Параметры backend http</span><span class="sxs-lookup"><span data-stu-id="eff9b-114">The backend http settings</span></span>

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

### <span data-ttu-id="eff9b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eff9b-115">-DefaultProfile</span></span>
<span data-ttu-id="eff9b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eff9b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eff9b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eff9b-117">CommonParameters</span></span>
<span data-ttu-id="eff9b-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eff9b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eff9b-119">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eff9b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eff9b-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eff9b-120">INPUTS</span></span>

### <span data-ttu-id="eff9b-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="eff9b-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="eff9b-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eff9b-122">OUTPUTS</span></span>

### <span data-ttu-id="eff9b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="eff9b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="eff9b-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eff9b-124">NOTES</span></span>

## <span data-ttu-id="eff9b-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eff9b-125">RELATED LINKS</span></span>

[<span data-ttu-id="eff9b-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eff9b-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)


[<span data-ttu-id="eff9b-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="eff9b-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="eff9b-128">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="eff9b-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="eff9b-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="eff9b-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

