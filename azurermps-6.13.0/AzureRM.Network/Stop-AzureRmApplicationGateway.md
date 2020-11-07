---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: a235ae8ad4467e135e85599300869bcb36805a30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732788"
---
# <span data-ttu-id="20c02-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="20c02-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="20c02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20c02-102">SYNOPSIS</span></span>
<span data-ttu-id="20c02-103">Остановка шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="20c02-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20c02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20c02-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20c02-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20c02-105">DESCRIPTION</span></span>
<span data-ttu-id="20c02-106">Командлет **Stop-AzureRmApplicationGateway** останавливает работу шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="20c02-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="20c02-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20c02-107">EXAMPLES</span></span>

### <span data-ttu-id="20c02-108">Пример 1: остановка шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="20c02-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="20c02-109">Эта команда останавливает шлюз приложения, хранящийся в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="20c02-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="20c02-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20c02-110">PARAMETERS</span></span>

### <span data-ttu-id="20c02-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="20c02-111">-ApplicationGateway</span></span>
<span data-ttu-id="20c02-112">Указывает шлюз приложений, который прекратит этот командлет.</span><span class="sxs-lookup"><span data-stu-id="20c02-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="20c02-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20c02-113">-AsJob</span></span>
<span data-ttu-id="20c02-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="20c02-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20c02-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c02-115">-DefaultProfile</span></span>
<span data-ttu-id="20c02-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="20c02-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20c02-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c02-117">CommonParameters</span></span>
<span data-ttu-id="20c02-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20c02-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c02-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20c02-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c02-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20c02-120">INPUTS</span></span>

### <span data-ttu-id="20c02-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="20c02-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="20c02-122">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="20c02-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="20c02-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20c02-123">OUTPUTS</span></span>

### <span data-ttu-id="20c02-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="20c02-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="20c02-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="20c02-125">NOTES</span></span>

## <span data-ttu-id="20c02-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20c02-126">RELATED LINKS</span></span>

[<span data-ttu-id="20c02-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="20c02-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="20c02-128">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="20c02-128">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="20c02-129">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="20c02-129">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="20c02-130">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="20c02-130">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="20c02-131">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="20c02-131">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


