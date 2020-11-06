---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: f9be647a4c6cb9d5198edcc766a20b3588e7626b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560103"
---
# <span data-ttu-id="f9a24-101">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9a24-101">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="f9a24-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f9a24-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a24-103">Получает конфигурацию автоматического масштабирования для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="f9a24-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9a24-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f9a24-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9a24-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9a24-105">DESCRIPTION</span></span>
<span data-ttu-id="f9a24-106">Командлет **Get-AzureRmApplicationGatewayAutoscaleConfiguration** получает конфигурацию автомасштабирования шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="f9a24-106">The **Get-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="f9a24-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f9a24-107">EXAMPLES</span></span>

### <span data-ttu-id="f9a24-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f9a24-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="f9a24-109">Первая команда получает шлюз приложения и сохраняет его в $gw переменной.</span><span class="sxs-lookup"><span data-stu-id="f9a24-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="f9a24-110">Вторая команда извлекает конфигурацию автомасштабирования из шлюза applicationg.</span><span class="sxs-lookup"><span data-stu-id="f9a24-110">The second command extracts out the autoscale configuration from the applicationg gateway.</span></span>

## <span data-ttu-id="f9a24-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f9a24-111">PARAMETERS</span></span>

### <span data-ttu-id="f9a24-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9a24-112">-ApplicationGateway</span></span>
<span data-ttu-id="f9a24-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9a24-113">The applicationGateway</span></span>

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

### <span data-ttu-id="f9a24-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9a24-114">-DefaultProfile</span></span>
<span data-ttu-id="f9a24-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f9a24-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9a24-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a24-116">CommonParameters</span></span>
<span data-ttu-id="f9a24-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f9a24-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a24-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9a24-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a24-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f9a24-119">INPUTS</span></span>

### <span data-ttu-id="f9a24-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9a24-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f9a24-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9a24-121">OUTPUTS</span></span>

### <span data-ttu-id="f9a24-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9a24-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="f9a24-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="f9a24-123">NOTES</span></span>

## <span data-ttu-id="f9a24-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9a24-124">RELATED LINKS</span></span>
