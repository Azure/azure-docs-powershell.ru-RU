---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: c3bc83f3f38c8a9b3c34e990e5729648a3677dd8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909550"
---
# <span data-ttu-id="b384f-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b384f-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b384f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b384f-102">SYNOPSIS</span></span>
<span data-ttu-id="b384f-103">Удаление прослушивателя HTTP из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b384f-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="b384f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b384f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b384f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b384f-105">DESCRIPTION</span></span>
<span data-ttu-id="b384f-106">Командлет **Remove-AzApplicationGatewayHttpListener** Удаляет прослушиватель HTTP из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="b384f-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="b384f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b384f-107">EXAMPLES</span></span>

### <span data-ttu-id="b384f-108">Пример 1: Удаление прослушивателя HTTP шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="b384f-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="b384f-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b384f-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="b384f-110">Вторая команда удаляет прослушиватель HTTP с именем Listener02 из шлюза приложения, который хранится в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b384f-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="b384f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b384f-111">PARAMETERS</span></span>

### <span data-ttu-id="b384f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b384f-112">-ApplicationGateway</span></span>
<span data-ttu-id="b384f-113">Указывает шлюз приложения, из которого нужно удалить прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="b384f-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="b384f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b384f-114">-DefaultProfile</span></span>
<span data-ttu-id="b384f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b384f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b384f-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b384f-116">-Name</span></span>
<span data-ttu-id="b384f-117">Указывает имя HTTP-прослушивателя, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="b384f-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b384f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b384f-118">CommonParameters</span></span>
<span data-ttu-id="b384f-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b384f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b384f-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b384f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b384f-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b384f-121">INPUTS</span></span>

### <span data-ttu-id="b384f-122">System. String</span><span class="sxs-lookup"><span data-stu-id="b384f-122">System.String</span></span>

## <span data-ttu-id="b384f-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b384f-123">OUTPUTS</span></span>

### <span data-ttu-id="b384f-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b384f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b384f-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="b384f-125">NOTES</span></span>

## <span data-ttu-id="b384f-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b384f-126">RELATED LINKS</span></span>

[<span data-ttu-id="b384f-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b384f-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b384f-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b384f-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b384f-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b384f-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b384f-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b384f-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


