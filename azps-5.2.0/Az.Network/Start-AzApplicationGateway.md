---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 974e30d9a287d18293515c019b0032bf36f15b51
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413663"
---
# <span data-ttu-id="4c973-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c973-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="4c973-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c973-102">SYNOPSIS</span></span>
<span data-ttu-id="4c973-103">Запускает шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="4c973-103">Starts an application gateway.</span></span>

## <span data-ttu-id="4c973-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4c973-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c973-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c973-105">DESCRIPTION</span></span>
<span data-ttu-id="4c973-106">Для **запуска шлюза приложения Azure запускается cmdlet Start-AzApplicationGateway**</span><span class="sxs-lookup"><span data-stu-id="4c973-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="4c973-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4c973-107">EXAMPLES</span></span>

### <span data-ttu-id="4c973-108">Пример 1. Запуск шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="4c973-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="4c973-109">Эта команда запускает шлюз приложения, который хранится в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4c973-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="4c973-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c973-110">PARAMETERS</span></span>

### <span data-ttu-id="4c973-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c973-111">-ApplicationGateway</span></span>
<span data-ttu-id="4c973-112">Указывает шлюз приложения, с который запускается этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c973-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="4c973-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c973-113">-DefaultProfile</span></span>
<span data-ttu-id="4c973-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c973-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c973-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c973-115">CommonParameters</span></span>
<span data-ttu-id="4c973-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c973-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c973-117">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c973-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c973-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c973-118">INPUTS</span></span>

### <span data-ttu-id="4c973-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c973-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4c973-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4c973-120">OUTPUTS</span></span>

### <span data-ttu-id="4c973-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c973-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4c973-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4c973-122">NOTES</span></span>

## <span data-ttu-id="4c973-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c973-123">RELATED LINKS</span></span>

[<span data-ttu-id="4c973-124">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c973-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


