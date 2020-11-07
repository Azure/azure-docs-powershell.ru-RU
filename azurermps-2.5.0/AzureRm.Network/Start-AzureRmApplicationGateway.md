---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 382c4cd1b189e0dc95edd4824dec58a280dbb889
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914382"
---
# <span data-ttu-id="9b6fc-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b6fc-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="9b6fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b6fc-102">SYNOPSIS</span></span>
<span data-ttu-id="9b6fc-103">Запускает шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="9b6fc-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b6fc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b6fc-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b6fc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b6fc-105">DESCRIPTION</span></span>
<span data-ttu-id="9b6fc-106">Командлет **Start-AzureRmApplicationGateway** запускает шлюз приложений Azure</span><span class="sxs-lookup"><span data-stu-id="9b6fc-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="9b6fc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b6fc-107">EXAMPLES</span></span>

### <span data-ttu-id="9b6fc-108">Example1: запуск шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="9b6fc-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="9b6fc-109">Эта команда запускает шлюз приложения, хранящийся в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9b6fc-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="9b6fc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b6fc-110">PARAMETERS</span></span>

### <span data-ttu-id="9b6fc-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b6fc-111">-ApplicationGateway</span></span>
<span data-ttu-id="9b6fc-112">Указывает шлюз приложений, с которого запускается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9b6fc-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="9b6fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b6fc-113">-DefaultProfile</span></span>
<span data-ttu-id="9b6fc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b6fc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b6fc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b6fc-115">CommonParameters</span></span>
<span data-ttu-id="9b6fc-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b6fc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b6fc-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b6fc-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b6fc-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b6fc-118">INPUTS</span></span>

### <span data-ttu-id="9b6fc-119">System. String</span><span class="sxs-lookup"><span data-stu-id="9b6fc-119">System.String</span></span>

## <span data-ttu-id="9b6fc-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b6fc-120">OUTPUTS</span></span>

### <span data-ttu-id="9b6fc-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b6fc-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9b6fc-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b6fc-122">NOTES</span></span>

## <span data-ttu-id="9b6fc-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b6fc-123">RELATED LINKS</span></span>

[<span data-ttu-id="9b6fc-124">Остановить-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b6fc-124">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


