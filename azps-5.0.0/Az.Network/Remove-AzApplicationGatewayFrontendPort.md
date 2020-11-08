---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: fe21bc83fce1e43e036f68ea64c8a10cf2f3c90e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248111"
---
# <span data-ttu-id="5af0c-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5af0c-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="5af0c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5af0c-102">SYNOPSIS</span></span>
<span data-ttu-id="5af0c-103">Удаляет интерфейсный порт из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="5af0c-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="5af0c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5af0c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5af0c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5af0c-105">DESCRIPTION</span></span>
<span data-ttu-id="5af0c-106">Командлет **Remove-AzApplicationGatewayFrontendPort** удаляет интерфейсный порт из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="5af0c-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="5af0c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5af0c-107">EXAMPLES</span></span>

### <span data-ttu-id="5af0c-108">Пример: Удаление порта переднего плана из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="5af0c-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="5af0c-109">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет шлюз в $AppGw переменной.</span><span class="sxs-lookup"><span data-stu-id="5af0c-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="5af0c-110">Вторая команда удаляет порт с именем FrontEndPort02 из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="5af0c-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="5af0c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5af0c-111">PARAMETERS</span></span>

### <span data-ttu-id="5af0c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5af0c-112">-ApplicationGateway</span></span>
<span data-ttu-id="5af0c-113">Указывает шлюз приложения, из которого нужно удалить порт переднего плана.</span><span class="sxs-lookup"><span data-stu-id="5af0c-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="5af0c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5af0c-114">-DefaultProfile</span></span>
<span data-ttu-id="5af0c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5af0c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5af0c-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5af0c-116">-Name</span></span>
<span data-ttu-id="5af0c-117">Указывает имя удаляемого порта переднего плана.</span><span class="sxs-lookup"><span data-stu-id="5af0c-117">Specifies name of the frontend port to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5af0c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5af0c-118">CommonParameters</span></span>
<span data-ttu-id="5af0c-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5af0c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5af0c-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5af0c-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5af0c-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5af0c-121">INPUTS</span></span>

### <span data-ttu-id="5af0c-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5af0c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5af0c-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5af0c-123">OUTPUTS</span></span>

### <span data-ttu-id="5af0c-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5af0c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5af0c-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="5af0c-125">NOTES</span></span>

## <span data-ttu-id="5af0c-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5af0c-126">RELATED LINKS</span></span>

[<span data-ttu-id="5af0c-127">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5af0c-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5af0c-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5af0c-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5af0c-129">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5af0c-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5af0c-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5af0c-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


