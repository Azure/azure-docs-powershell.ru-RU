---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: a60fa54e5d705a71407f2c56986200c897b838e3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913779"
---
# <span data-ttu-id="bcb17-101">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bcb17-101">Remove-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="bcb17-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bcb17-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb17-103">Удаление прослушивателя HTTP из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="bcb17-103">Removes an HTTP listener from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcb17-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bcb17-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcb17-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcb17-105">DESCRIPTION</span></span>
<span data-ttu-id="bcb17-106">Командлет **Remove-AzureRmApplicationGatewayHttpListener** Удаляет прослушиватель HTTP из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb17-106">The **Remove-AzureRmApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="bcb17-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bcb17-107">EXAMPLES</span></span>

### <span data-ttu-id="bcb17-108">Пример 1: Удаление прослушивателя HTTP шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="bcb17-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="bcb17-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="bcb17-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="bcb17-110">Вторая команда удаляет прослушиватель HTTP с именем Listener02 из шлюза приложения, который хранится в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="bcb17-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="bcb17-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bcb17-111">PARAMETERS</span></span>

### <span data-ttu-id="bcb17-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bcb17-112">-ApplicationGateway</span></span>
<span data-ttu-id="bcb17-113">Указывает шлюз приложения, из которого нужно удалить прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="bcb17-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="bcb17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb17-114">-DefaultProfile</span></span>
<span data-ttu-id="bcb17-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb17-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcb17-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bcb17-116">-Name</span></span>
<span data-ttu-id="bcb17-117">Указывает имя HTTP-прослушивателя, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="bcb17-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bcb17-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb17-118">CommonParameters</span></span>
<span data-ttu-id="bcb17-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bcb17-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb17-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcb17-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb17-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bcb17-121">INPUTS</span></span>

### <span data-ttu-id="bcb17-122">System. String</span><span class="sxs-lookup"><span data-stu-id="bcb17-122">System.String</span></span>

## <span data-ttu-id="bcb17-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcb17-123">OUTPUTS</span></span>

### <span data-ttu-id="bcb17-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bcb17-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="bcb17-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="bcb17-125">NOTES</span></span>

## <span data-ttu-id="bcb17-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bcb17-126">RELATED LINKS</span></span>

[<span data-ttu-id="bcb17-127">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bcb17-127">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="bcb17-128">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bcb17-128">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="bcb17-129">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bcb17-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="bcb17-130">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bcb17-130">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


