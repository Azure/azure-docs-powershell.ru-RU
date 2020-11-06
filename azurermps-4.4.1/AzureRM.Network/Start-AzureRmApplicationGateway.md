---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
ms.openlocfilehash: 8d6f52401544d723f7f5303aa45722d828a6ac59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559611"
---
# <span data-ttu-id="7228a-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7228a-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="7228a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7228a-102">SYNOPSIS</span></span>
<span data-ttu-id="7228a-103">Запускает шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="7228a-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7228a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7228a-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7228a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7228a-105">DESCRIPTION</span></span>
<span data-ttu-id="7228a-106">Командлет **Start-AzureRmApplicationGateway** запускает шлюз приложений Azure</span><span class="sxs-lookup"><span data-stu-id="7228a-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="7228a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7228a-107">EXAMPLES</span></span>

### <span data-ttu-id="7228a-108">Example1: запуск шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="7228a-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="7228a-109">Эта команда запускает шлюз приложения, хранящийся в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7228a-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="7228a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7228a-110">PARAMETERS</span></span>

### <span data-ttu-id="7228a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7228a-111">-ApplicationGateway</span></span>
<span data-ttu-id="7228a-112">Указывает шлюз приложений, с которого запускается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7228a-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="7228a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7228a-113">-DefaultProfile</span></span>
<span data-ttu-id="7228a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7228a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7228a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7228a-115">CommonParameters</span></span>
<span data-ttu-id="7228a-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7228a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7228a-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7228a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7228a-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7228a-118">INPUTS</span></span>

### <span data-ttu-id="7228a-119">System. String</span><span class="sxs-lookup"><span data-stu-id="7228a-119">System.String</span></span>

## <span data-ttu-id="7228a-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7228a-120">OUTPUTS</span></span>

### <span data-ttu-id="7228a-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7228a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7228a-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="7228a-122">NOTES</span></span>

## <span data-ttu-id="7228a-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7228a-123">RELATED LINKS</span></span>

[<span data-ttu-id="7228a-124">Остановить-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7228a-124">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


