---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 67652681b5a0cf5468fa42fb9090446f2a11158e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910074"
---
# <span data-ttu-id="d282a-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d282a-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="d282a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d282a-102">SYNOPSIS</span></span>
<span data-ttu-id="d282a-103">Получает HTTP-прослушиватель для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="d282a-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="d282a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d282a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d282a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d282a-105">DESCRIPTION</span></span>
<span data-ttu-id="d282a-106">Командлет **Get-AzApplicationGatewayHttpListener** получает HTTP-прослушиватель для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="d282a-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="d282a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d282a-107">EXAMPLES</span></span>

### <span data-ttu-id="d282a-108">Пример 1: получение определенного HTTP-прослушивателя</span><span class="sxs-lookup"><span data-stu-id="d282a-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="d282a-109">Эта команда получает прослушиватель HTTP с именем Listener01.</span><span class="sxs-lookup"><span data-stu-id="d282a-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="d282a-110">Пример 2: получение списка прослушивателей HTTP</span><span class="sxs-lookup"><span data-stu-id="d282a-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="d282a-111">Эта команда получает список прослушивателей HTTP.</span><span class="sxs-lookup"><span data-stu-id="d282a-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="d282a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d282a-112">PARAMETERS</span></span>

### <span data-ttu-id="d282a-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d282a-113">-ApplicationGateway</span></span>
<span data-ttu-id="d282a-114">Указывает объект шлюза приложения, который содержит прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="d282a-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="d282a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d282a-115">-DefaultProfile</span></span>
<span data-ttu-id="d282a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d282a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d282a-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d282a-117">-Name</span></span>
<span data-ttu-id="d282a-118">Указывает имя прослушивателя HTTP, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d282a-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="d282a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d282a-119">CommonParameters</span></span>
<span data-ttu-id="d282a-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d282a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d282a-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d282a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d282a-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d282a-122">INPUTS</span></span>

### <span data-ttu-id="d282a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d282a-123">System.String</span></span>

## <span data-ttu-id="d282a-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d282a-124">OUTPUTS</span></span>

### <span data-ttu-id="d282a-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d282a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="d282a-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="d282a-126">NOTES</span></span>

## <span data-ttu-id="d282a-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d282a-127">RELATED LINKS</span></span>

[<span data-ttu-id="d282a-128">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d282a-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="d282a-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d282a-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="d282a-130">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d282a-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="d282a-131">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d282a-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


