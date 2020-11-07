---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: f90e35e0b8a88d7fa7b5089adf205bf6fe14e18f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729946"
---
# <span data-ttu-id="f34b5-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f34b5-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="f34b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f34b5-102">SYNOPSIS</span></span>
<span data-ttu-id="f34b5-103">Запускает шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="f34b5-103">Starts an application gateway.</span></span>

## <span data-ttu-id="f34b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f34b5-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f34b5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f34b5-105">DESCRIPTION</span></span>
<span data-ttu-id="f34b5-106">Командлет **Start-AzApplicationGateway** запускает шлюз приложений Azure</span><span class="sxs-lookup"><span data-stu-id="f34b5-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="f34b5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f34b5-107">EXAMPLES</span></span>

### <span data-ttu-id="f34b5-108">Example1: запуск шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="f34b5-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="f34b5-109">Эта команда запускает шлюз приложения, хранящийся в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f34b5-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="f34b5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f34b5-110">PARAMETERS</span></span>

### <span data-ttu-id="f34b5-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f34b5-111">-ApplicationGateway</span></span>
<span data-ttu-id="f34b5-112">Указывает шлюз приложений, с которого запускается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f34b5-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="f34b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f34b5-113">-DefaultProfile</span></span>
<span data-ttu-id="f34b5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f34b5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f34b5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f34b5-115">CommonParameters</span></span>
<span data-ttu-id="f34b5-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f34b5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f34b5-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f34b5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f34b5-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f34b5-118">INPUTS</span></span>

### <span data-ttu-id="f34b5-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f34b5-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f34b5-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f34b5-120">OUTPUTS</span></span>

### <span data-ttu-id="f34b5-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f34b5-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f34b5-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="f34b5-122">NOTES</span></span>

## <span data-ttu-id="f34b5-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f34b5-123">RELATED LINKS</span></span>

[<span data-ttu-id="f34b5-124">Остановить-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f34b5-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


