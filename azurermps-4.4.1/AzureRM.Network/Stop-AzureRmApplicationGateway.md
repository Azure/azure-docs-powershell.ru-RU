---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: 6c2de883a797c445105edddfc562bc2d494fd234
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559608"
---
# <span data-ttu-id="d58aa-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d58aa-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="d58aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d58aa-102">SYNOPSIS</span></span>
<span data-ttu-id="d58aa-103">Остановка шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="d58aa-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d58aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d58aa-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d58aa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d58aa-105">DESCRIPTION</span></span>
<span data-ttu-id="d58aa-106">Командлет **Stop-AzureRmApplicationGateway** останавливает работу шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="d58aa-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="d58aa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d58aa-107">EXAMPLES</span></span>

### <span data-ttu-id="d58aa-108">Пример 1: остановка шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="d58aa-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="d58aa-109">Эта команда останавливает шлюз приложения, хранящийся в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d58aa-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="d58aa-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d58aa-110">PARAMETERS</span></span>

### <span data-ttu-id="d58aa-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d58aa-111">-ApplicationGateway</span></span>
<span data-ttu-id="d58aa-112">Указывает шлюз приложений, который прекратит этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d58aa-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="d58aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d58aa-113">-DefaultProfile</span></span>
<span data-ttu-id="d58aa-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d58aa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d58aa-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d58aa-115">CommonParameters</span></span>
<span data-ttu-id="d58aa-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d58aa-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d58aa-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d58aa-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d58aa-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d58aa-118">INPUTS</span></span>

### <span data-ttu-id="d58aa-119">System. String</span><span class="sxs-lookup"><span data-stu-id="d58aa-119">System.String</span></span>

## <span data-ttu-id="d58aa-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d58aa-120">OUTPUTS</span></span>

### <span data-ttu-id="d58aa-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d58aa-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d58aa-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="d58aa-122">NOTES</span></span>

## <span data-ttu-id="d58aa-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d58aa-123">RELATED LINKS</span></span>

[<span data-ttu-id="d58aa-124">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d58aa-124">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="d58aa-125">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d58aa-125">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="d58aa-126">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d58aa-126">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="d58aa-127">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d58aa-127">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="d58aa-128">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d58aa-128">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


