---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: c9ebdbf6feec64cc4545b1a77b39d91d4bf98d79
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073568"
---
# <span data-ttu-id="ef217-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ef217-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="ef217-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef217-102">SYNOPSIS</span></span>
<span data-ttu-id="ef217-103">Возвращает конфигурацию сток подключений для объекта параметров HTTP с внутренним интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="ef217-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="ef217-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef217-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef217-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef217-105">DESCRIPTION</span></span>
<span data-ttu-id="ef217-106">Командлет **Get-AzApplicationGatewayConnectionDraining** возвращает конфигурацию сток подключений для объекта параметров HTTP с внутренним интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="ef217-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="ef217-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef217-107">EXAMPLES</span></span>

### <span data-ttu-id="ef217-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ef217-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="ef217-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ef217-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ef217-110">Вторая команда получает серверные параметры HTTP с именем Settings01 для $AppGw и сохраняет параметры в переменной $Settings.</span><span class="sxs-lookup"><span data-stu-id="ef217-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="ef217-111">Последняя команда получает конфигурацию сток подключений из параметров HTTP для заднего элемента $Settings и сохраняет ее в переменной $ConnectionDraining.</span><span class="sxs-lookup"><span data-stu-id="ef217-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="ef217-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef217-112">PARAMETERS</span></span>

### <span data-ttu-id="ef217-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ef217-113">-BackendHttpSettings</span></span>
<span data-ttu-id="ef217-114">Параметры внутренних HTTP-данных</span><span class="sxs-lookup"><span data-stu-id="ef217-114">The backend http settings</span></span>

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

### <span data-ttu-id="ef217-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef217-115">-DefaultProfile</span></span>
<span data-ttu-id="ef217-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef217-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef217-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef217-117">CommonParameters</span></span>
<span data-ttu-id="ef217-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef217-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef217-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef217-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef217-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef217-120">INPUTS</span></span>

### <span data-ttu-id="ef217-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ef217-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="ef217-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef217-122">OUTPUTS</span></span>

### <span data-ttu-id="ef217-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ef217-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="ef217-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef217-124">NOTES</span></span>

## <span data-ttu-id="ef217-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef217-125">RELATED LINKS</span></span>

[<span data-ttu-id="ef217-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef217-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="ef217-127">Get-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ef217-127">Get-AzApplicationGatewayBackendHttpSettings</span></span>](./Get-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="ef217-128">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ef217-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="ef217-129">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ef217-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="ef217-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ef217-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
