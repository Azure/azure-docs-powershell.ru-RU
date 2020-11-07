---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
ms.openlocfilehash: 475a3bf32507267b35808964e35af112dfdff928
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913847"
---
# <span data-ttu-id="7caea-101">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7caea-101">Get-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="7caea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7caea-102">SYNOPSIS</span></span>
<span data-ttu-id="7caea-103">Возвращает конфигурацию сток подключений для объекта параметров HTTP с внутренним интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="7caea-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7caea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7caea-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7caea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7caea-105">DESCRIPTION</span></span>
<span data-ttu-id="7caea-106">Командлет **Get-AzureRmApplicationGatewayConnectionDraining** возвращает конфигурацию сток подключений для объекта параметров HTTP с внутренним интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="7caea-106">The **Get-AzureRmApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="7caea-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7caea-107">EXAMPLES</span></span>

### <span data-ttu-id="7caea-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7caea-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="7caea-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7caea-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7caea-110">Вторая команда получает серверные параметры HTTP с именем Settings01 для $AppGw и сохраняет параметры в переменной $Settings.</span><span class="sxs-lookup"><span data-stu-id="7caea-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="7caea-111">Последняя команда получает конфигурацию сток подключений из параметров HTTP для заднего элемента $Settings и сохраняет ее в переменной $ConnectionDraining.</span><span class="sxs-lookup"><span data-stu-id="7caea-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="7caea-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7caea-112">PARAMETERS</span></span>

### <span data-ttu-id="7caea-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7caea-113">-BackendHttpSettings</span></span>
<span data-ttu-id="7caea-114">Параметры внутренних HTTP-данных</span><span class="sxs-lookup"><span data-stu-id="7caea-114">The backend http settings</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7caea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7caea-115">-DefaultProfile</span></span>
<span data-ttu-id="7caea-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7caea-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7caea-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7caea-117">CommonParameters</span></span>
<span data-ttu-id="7caea-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7caea-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7caea-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7caea-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7caea-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7caea-120">INPUTS</span></span>

### <span data-ttu-id="7caea-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7caea-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="7caea-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7caea-122">OUTPUTS</span></span>

### <span data-ttu-id="7caea-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7caea-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="7caea-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="7caea-124">NOTES</span></span>

## <span data-ttu-id="7caea-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7caea-125">RELATED LINKS</span></span>

[<span data-ttu-id="7caea-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7caea-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="7caea-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7caea-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="7caea-128">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7caea-128">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="7caea-129">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7caea-129">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="7caea-130">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7caea-130">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)
