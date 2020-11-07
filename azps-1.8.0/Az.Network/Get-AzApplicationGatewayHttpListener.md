---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 91b2791b7f61c7586c1fbd4bca954e374ccbb43c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730648"
---
# <span data-ttu-id="0f359-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0f359-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="0f359-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f359-102">SYNOPSIS</span></span>
<span data-ttu-id="0f359-103">Получает HTTP-прослушиватель для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="0f359-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="0f359-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f359-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f359-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f359-105">DESCRIPTION</span></span>
<span data-ttu-id="0f359-106">Командлет **Get-AzApplicationGatewayHttpListener** получает HTTP-прослушиватель для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="0f359-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="0f359-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f359-107">EXAMPLES</span></span>

### <span data-ttu-id="0f359-108">Пример 1: получение определенного HTTP-прослушивателя</span><span class="sxs-lookup"><span data-stu-id="0f359-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="0f359-109">Эта команда получает прослушиватель HTTP с именем Listener01.</span><span class="sxs-lookup"><span data-stu-id="0f359-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="0f359-110">Пример 2: получение списка прослушивателей HTTP</span><span class="sxs-lookup"><span data-stu-id="0f359-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="0f359-111">Эта команда получает список прослушивателей HTTP.</span><span class="sxs-lookup"><span data-stu-id="0f359-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="0f359-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f359-112">PARAMETERS</span></span>

### <span data-ttu-id="0f359-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0f359-113">-ApplicationGateway</span></span>
<span data-ttu-id="0f359-114">Указывает объект шлюза приложения, который содержит прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="0f359-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="0f359-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f359-115">-DefaultProfile</span></span>
<span data-ttu-id="0f359-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f359-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f359-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f359-117">-Name</span></span>
<span data-ttu-id="0f359-118">Указывает имя прослушивателя HTTP, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0f359-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="0f359-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f359-119">CommonParameters</span></span>
<span data-ttu-id="0f359-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f359-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f359-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f359-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f359-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f359-122">INPUTS</span></span>

### <span data-ttu-id="0f359-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0f359-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0f359-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f359-124">OUTPUTS</span></span>

### <span data-ttu-id="0f359-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0f359-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="0f359-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f359-126">NOTES</span></span>

## <span data-ttu-id="0f359-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f359-127">RELATED LINKS</span></span>

[<span data-ttu-id="0f359-128">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0f359-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="0f359-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0f359-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="0f359-130">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0f359-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="0f359-131">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0f359-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


