---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 2b35d3978859c65ec5219fe3e0208776d7dc7d68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568572"
---
# <span data-ttu-id="62b77-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="62b77-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="62b77-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62b77-102">SYNOPSIS</span></span>
<span data-ttu-id="62b77-103">Получает существующую конфигурацию перенаправления из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="62b77-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62b77-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62b77-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62b77-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62b77-105">DESCRIPTION</span></span>
<span data-ttu-id="62b77-106">Командлет **Get-AzureRmApplicationGatewayRedirectConfiguration** получает существующую конфигурацию перенаправления из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="62b77-106">The **Get-AzureRmApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="62b77-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62b77-107">EXAMPLES</span></span>

### <span data-ttu-id="62b77-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62b77-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="62b77-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="62b77-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="62b77-110">Вторая команда получает конфигурацию перенаправления с именем Redirect01 из шлюза приложения, который хранится в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="62b77-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="62b77-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62b77-111">PARAMETERS</span></span>

### <span data-ttu-id="62b77-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62b77-112">-ApplicationGateway</span></span>
<span data-ttu-id="62b77-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62b77-113">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62b77-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b77-114">-DefaultProfile</span></span>
<span data-ttu-id="62b77-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62b77-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62b77-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="62b77-116">-Name</span></span>
<span data-ttu-id="62b77-117">Имя правила маршрутизации запросов</span><span class="sxs-lookup"><span data-stu-id="62b77-117">The name of the request routing rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62b77-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b77-118">CommonParameters</span></span>
<span data-ttu-id="62b77-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62b77-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b77-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62b77-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b77-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62b77-121">INPUTS</span></span>

### <span data-ttu-id="62b77-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62b77-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="62b77-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62b77-123">OUTPUTS</span></span>

### <span data-ttu-id="62b77-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="62b77-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>
<span data-ttu-id="62b77-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. rePSApplicationGatewayRedirectConfiguration, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="62b77-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="62b77-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="62b77-126">NOTES</span></span>

## <span data-ttu-id="62b77-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62b77-127">RELATED LINKS</span></span>

