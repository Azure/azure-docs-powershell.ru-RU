---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 8c37ed72659c8b5ab00d54a7ecbe9622cb9f553b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910994"
---
# <span data-ttu-id="6b68a-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b68a-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="6b68a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b68a-102">SYNOPSIS</span></span>
<span data-ttu-id="6b68a-103">Запускает шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="6b68a-103">Starts an application gateway.</span></span>

## <span data-ttu-id="6b68a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b68a-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b68a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b68a-105">DESCRIPTION</span></span>
<span data-ttu-id="6b68a-106">Командлет **Start-AzApplicationGateway** запускает шлюз приложений Azure</span><span class="sxs-lookup"><span data-stu-id="6b68a-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="6b68a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b68a-107">EXAMPLES</span></span>

### <span data-ttu-id="6b68a-108">Example1: запуск шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="6b68a-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="6b68a-109">Эта команда запускает шлюз приложения, хранящийся в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="6b68a-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="6b68a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b68a-110">PARAMETERS</span></span>

### <span data-ttu-id="6b68a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b68a-111">-ApplicationGateway</span></span>
<span data-ttu-id="6b68a-112">Указывает шлюз приложений, с которого запускается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6b68a-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="6b68a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b68a-113">-DefaultProfile</span></span>
<span data-ttu-id="6b68a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b68a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b68a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b68a-115">CommonParameters</span></span>
<span data-ttu-id="6b68a-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b68a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b68a-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b68a-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b68a-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b68a-118">INPUTS</span></span>

### <span data-ttu-id="6b68a-119">System. String</span><span class="sxs-lookup"><span data-stu-id="6b68a-119">System.String</span></span>

## <span data-ttu-id="6b68a-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b68a-120">OUTPUTS</span></span>

### <span data-ttu-id="6b68a-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b68a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6b68a-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b68a-122">NOTES</span></span>

## <span data-ttu-id="6b68a-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b68a-123">RELATED LINKS</span></span>

[<span data-ttu-id="6b68a-124">Остановить-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b68a-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


