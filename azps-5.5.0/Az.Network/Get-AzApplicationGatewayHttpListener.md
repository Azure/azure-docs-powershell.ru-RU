---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 30f47cf6e345710da0e0d626929f65a33490e246
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241061"
---
# <span data-ttu-id="cb081-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="cb081-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="cb081-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb081-102">SYNOPSIS</span></span>
<span data-ttu-id="cb081-103">Получение программы HTTP-прослушивания шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="cb081-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="cb081-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cb081-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb081-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb081-105">DESCRIPTION</span></span>
<span data-ttu-id="cb081-106">С **помощью cmdlet Get-AzApplicationGatewayHttpListener** можно получить http-прослушивание шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="cb081-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="cb081-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cb081-107">EXAMPLES</span></span>

### <span data-ttu-id="cb081-108">Пример 1. Укайл конкретного http-прослушивание</span><span class="sxs-lookup"><span data-stu-id="cb081-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="cb081-109">Эта команда получает http-прослушивание с именем Listener01.</span><span class="sxs-lookup"><span data-stu-id="cb081-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="cb081-110">Пример 2. Получить список http-загона</span><span class="sxs-lookup"><span data-stu-id="cb081-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="cb081-111">Эта команда возвращает список http-версий.</span><span class="sxs-lookup"><span data-stu-id="cb081-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="cb081-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb081-112">PARAMETERS</span></span>

### <span data-ttu-id="cb081-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb081-113">-ApplicationGateway</span></span>
<span data-ttu-id="cb081-114">Указывает объект шлюза приложения, содержащий http-прослушивание.</span><span class="sxs-lookup"><span data-stu-id="cb081-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="cb081-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb081-115">-DefaultProfile</span></span>
<span data-ttu-id="cb081-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb081-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb081-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cb081-117">-Name</span></span>
<span data-ttu-id="cb081-118">Указывает имя http-прослушивание, которое получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb081-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb081-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb081-119">CommonParameters</span></span>
<span data-ttu-id="cb081-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb081-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb081-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb081-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb081-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb081-122">INPUTS</span></span>

### <span data-ttu-id="cb081-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb081-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cb081-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cb081-124">OUTPUTS</span></span>

### <span data-ttu-id="cb081-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="cb081-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="cb081-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cb081-126">NOTES</span></span>

## <span data-ttu-id="cb081-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb081-127">RELATED LINKS</span></span>

[<span data-ttu-id="cb081-128">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="cb081-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="cb081-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="cb081-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="cb081-130">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="cb081-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="cb081-131">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="cb081-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


