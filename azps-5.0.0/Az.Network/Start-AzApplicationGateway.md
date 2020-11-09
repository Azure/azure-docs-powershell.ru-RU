---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 974e30d9a287d18293515c019b0032bf36f15b51
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319046"
---
# <span data-ttu-id="6f0db-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f0db-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="6f0db-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f0db-102">SYNOPSIS</span></span>
<span data-ttu-id="6f0db-103">Запускает шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="6f0db-103">Starts an application gateway.</span></span>

## <span data-ttu-id="6f0db-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f0db-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f0db-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f0db-105">DESCRIPTION</span></span>
<span data-ttu-id="6f0db-106">Командлет **Start-AzApplicationGateway** запускает шлюз приложений Azure</span><span class="sxs-lookup"><span data-stu-id="6f0db-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="6f0db-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f0db-107">EXAMPLES</span></span>

### <span data-ttu-id="6f0db-108">Example1: запуск шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="6f0db-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="6f0db-109">Эта команда запускает шлюз приложения, хранящийся в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="6f0db-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="6f0db-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f0db-110">PARAMETERS</span></span>

### <span data-ttu-id="6f0db-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f0db-111">-ApplicationGateway</span></span>
<span data-ttu-id="6f0db-112">Указывает шлюз приложений, с которого запускается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6f0db-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="6f0db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f0db-113">-DefaultProfile</span></span>
<span data-ttu-id="6f0db-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f0db-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f0db-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f0db-115">CommonParameters</span></span>
<span data-ttu-id="6f0db-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f0db-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f0db-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f0db-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f0db-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f0db-118">INPUTS</span></span>

### <span data-ttu-id="6f0db-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f0db-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6f0db-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f0db-120">OUTPUTS</span></span>

### <span data-ttu-id="6f0db-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f0db-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6f0db-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f0db-122">NOTES</span></span>

## <span data-ttu-id="6f0db-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f0db-123">RELATED LINKS</span></span>

[<span data-ttu-id="6f0db-124">Остановить-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f0db-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


