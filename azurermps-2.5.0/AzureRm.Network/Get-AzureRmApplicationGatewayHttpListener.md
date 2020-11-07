---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: 79b61f5d96307afea47851b210fc1a1ee97acf61
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914433"
---
# <span data-ttu-id="88c8c-101">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="88c8c-101">Get-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="88c8c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88c8c-102">SYNOPSIS</span></span>
<span data-ttu-id="88c8c-103">Получает HTTP-прослушиватель для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="88c8c-103">Gets the HTTP listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88c8c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88c8c-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88c8c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88c8c-105">DESCRIPTION</span></span>
<span data-ttu-id="88c8c-106">Командлет **Get-AzureRmApplicationGatewayHttpListener** получает HTTP-прослушиватель для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="88c8c-106">The **Get-AzureRmApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="88c8c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88c8c-107">EXAMPLES</span></span>

### <span data-ttu-id="88c8c-108">Пример 1: получение определенного HTTP-прослушивателя</span><span class="sxs-lookup"><span data-stu-id="88c8c-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzureRmApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="88c8c-109">Эта команда получает прослушиватель HTTP с именем Listener01.</span><span class="sxs-lookup"><span data-stu-id="88c8c-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="88c8c-110">Пример 2: получение списка прослушивателей HTTP</span><span class="sxs-lookup"><span data-stu-id="88c8c-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzureRmApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="88c8c-111">Эта команда получает список прослушивателей HTTP.</span><span class="sxs-lookup"><span data-stu-id="88c8c-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="88c8c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88c8c-112">PARAMETERS</span></span>

### <span data-ttu-id="88c8c-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="88c8c-113">-ApplicationGateway</span></span>
<span data-ttu-id="88c8c-114">Указывает объект шлюза приложения, который содержит прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="88c8c-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="88c8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88c8c-115">-DefaultProfile</span></span>
<span data-ttu-id="88c8c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88c8c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88c8c-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88c8c-117">-Name</span></span>
<span data-ttu-id="88c8c-118">Указывает имя прослушивателя HTTP, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="88c8c-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88c8c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88c8c-119">CommonParameters</span></span>
<span data-ttu-id="88c8c-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88c8c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88c8c-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88c8c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88c8c-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88c8c-122">INPUTS</span></span>

### <span data-ttu-id="88c8c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="88c8c-123">System.String</span></span>

## <span data-ttu-id="88c8c-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88c8c-124">OUTPUTS</span></span>

### <span data-ttu-id="88c8c-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="88c8c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="88c8c-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="88c8c-126">NOTES</span></span>

## <span data-ttu-id="88c8c-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88c8c-127">RELATED LINKS</span></span>

[<span data-ttu-id="88c8c-128">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="88c8c-128">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="88c8c-129">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="88c8c-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="88c8c-130">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="88c8c-130">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="88c8c-131">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="88c8c-131">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


