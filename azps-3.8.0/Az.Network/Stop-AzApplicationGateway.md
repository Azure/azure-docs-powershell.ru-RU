---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 4c7001bf69e6dc8f418f1bc56867154bf9d769ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911922"
---
# <span data-ttu-id="30286-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30286-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="30286-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30286-102">SYNOPSIS</span></span>
<span data-ttu-id="30286-103">Остановка шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="30286-103">Stops an application gateway</span></span>

## <span data-ttu-id="30286-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30286-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30286-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30286-105">DESCRIPTION</span></span>
<span data-ttu-id="30286-106">Командлет **Stop-AzApplicationGateway** останавливает работу шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="30286-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="30286-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30286-107">EXAMPLES</span></span>

### <span data-ttu-id="30286-108">Пример 1: остановка шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="30286-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="30286-109">Эта команда останавливает шлюз приложения, хранящийся в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="30286-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="30286-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30286-110">PARAMETERS</span></span>

### <span data-ttu-id="30286-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30286-111">-ApplicationGateway</span></span>
<span data-ttu-id="30286-112">Указывает шлюз приложений, который прекратит этот командлет.</span><span class="sxs-lookup"><span data-stu-id="30286-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="30286-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30286-113">-AsJob</span></span>
<span data-ttu-id="30286-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="30286-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30286-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30286-115">-DefaultProfile</span></span>
<span data-ttu-id="30286-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30286-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30286-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30286-117">CommonParameters</span></span>
<span data-ttu-id="30286-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30286-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30286-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30286-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30286-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30286-120">INPUTS</span></span>

### <span data-ttu-id="30286-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30286-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="30286-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30286-122">OUTPUTS</span></span>

### <span data-ttu-id="30286-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30286-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="30286-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="30286-124">NOTES</span></span>

## <span data-ttu-id="30286-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30286-125">RELATED LINKS</span></span>

[<span data-ttu-id="30286-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30286-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="30286-127">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30286-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="30286-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30286-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="30286-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30286-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="30286-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30286-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


