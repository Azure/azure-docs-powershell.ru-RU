---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 342b8e73ff4e3b01cbf51ea567e8eb7490ecd5c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066511"
---
# <span data-ttu-id="f77be-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f77be-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="f77be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f77be-102">SYNOPSIS</span></span>
<span data-ttu-id="f77be-103">Удаляет конфигурацию сток подключений для серверного объекта параметров HTTP.</span><span class="sxs-lookup"><span data-stu-id="f77be-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="f77be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f77be-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f77be-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f77be-105">DESCRIPTION</span></span>
<span data-ttu-id="f77be-106">Командлет **Remove-AzApplicationGatewayConnectionDraining** удаляет конфигурацию сток подключений для серверного объекта параметров HTTP.</span><span class="sxs-lookup"><span data-stu-id="f77be-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="f77be-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f77be-107">EXAMPLES</span></span>

### <span data-ttu-id="f77be-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f77be-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="f77be-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f77be-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f77be-110">Вторая команда получает серверные параметры HTTP с именем Settings01 для $AppGw и сохраняет параметры в переменной $Settings.</span><span class="sxs-lookup"><span data-stu-id="f77be-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="f77be-111">Последняя команда удаляет конфигурацию сток подключений для серверных параметров HTTP, хранящихся в $Settings.</span><span class="sxs-lookup"><span data-stu-id="f77be-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="f77be-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f77be-112">PARAMETERS</span></span>

### <span data-ttu-id="f77be-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f77be-113">-BackendHttpSettings</span></span>
<span data-ttu-id="f77be-114">Параметры внутренних HTTP-данных</span><span class="sxs-lookup"><span data-stu-id="f77be-114">The backend http settings</span></span>

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

### <span data-ttu-id="f77be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f77be-115">-DefaultProfile</span></span>
<span data-ttu-id="f77be-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f77be-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f77be-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f77be-117">CommonParameters</span></span>
<span data-ttu-id="f77be-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f77be-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f77be-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f77be-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f77be-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f77be-120">INPUTS</span></span>

### <span data-ttu-id="f77be-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f77be-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="f77be-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f77be-122">OUTPUTS</span></span>

### <span data-ttu-id="f77be-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f77be-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="f77be-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="f77be-124">NOTES</span></span>

## <span data-ttu-id="f77be-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f77be-125">RELATED LINKS</span></span>

[<span data-ttu-id="f77be-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f77be-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="f77be-127">Get-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f77be-127">Get-AzApplicationGatewayBackendHttpSettings</span></span>](./Get-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="f77be-128">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f77be-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="f77be-129">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f77be-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="f77be-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f77be-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

