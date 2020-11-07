---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3a25db38f26fe1714035acebba1063303cdc0934
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733031"
---
# <span data-ttu-id="ee95a-101">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="ee95a-101">Get-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="ee95a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee95a-102">SYNOPSIS</span></span>
<span data-ttu-id="ee95a-103">Возвращает политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="ee95a-103">Gets the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee95a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee95a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee95a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee95a-105">DESCRIPTION</span></span>
<span data-ttu-id="ee95a-106">Командлет **Get-AzureRmApplicationGatewaySslPolicy** получает политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="ee95a-106">The **Get-AzureRmApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="ee95a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee95a-107">EXAMPLES</span></span>

### <span data-ttu-id="ee95a-108">1:</span><span class="sxs-lookup"><span data-stu-id="ee95a-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="ee95a-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="ee95a-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="ee95a-110">Вторая команда получает политику SSL из шлюза приложения, который хранится в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="ee95a-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="ee95a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee95a-111">PARAMETERS</span></span>

### <span data-ttu-id="ee95a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ee95a-112">-ApplicationGateway</span></span>
<span data-ttu-id="ee95a-113">Указывает шлюз приложения политики SSL, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ee95a-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ee95a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee95a-114">-DefaultProfile</span></span>
<span data-ttu-id="ee95a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee95a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee95a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee95a-116">CommonParameters</span></span>
<span data-ttu-id="ee95a-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee95a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee95a-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee95a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee95a-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee95a-119">INPUTS</span></span>

### <span data-ttu-id="ee95a-120">System. String</span><span class="sxs-lookup"><span data-stu-id="ee95a-120">System.String</span></span>

## <span data-ttu-id="ee95a-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee95a-121">OUTPUTS</span></span>

### <span data-ttu-id="ee95a-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="ee95a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="ee95a-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee95a-123">NOTES</span></span>
* <span data-ttu-id="ee95a-124">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="ee95a-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ee95a-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee95a-125">RELATED LINKS</span></span>

[<span data-ttu-id="ee95a-126">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="ee95a-126">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="ee95a-127">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="ee95a-127">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


