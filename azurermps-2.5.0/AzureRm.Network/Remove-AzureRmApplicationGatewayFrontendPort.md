---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendport
schema: 2.0.0
ms.openlocfilehash: ecee205ee831c5ba7a2fa78c00f005af3303a13a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913607"
---
# <span data-ttu-id="b25aa-101">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b25aa-101">Remove-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="b25aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b25aa-102">SYNOPSIS</span></span>
<span data-ttu-id="b25aa-103">Удаляет интерфейсный порт из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b25aa-103">Removes a front-end port from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b25aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b25aa-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b25aa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b25aa-105">DESCRIPTION</span></span>
<span data-ttu-id="b25aa-106">Командлет **Remove-AzureRmApplicationGatewayFrontendPort** удаляет интерфейсный порт из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="b25aa-106">The **Remove-AzureRmApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="b25aa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b25aa-107">EXAMPLES</span></span>

### <span data-ttu-id="b25aa-108">Пример: Удаление порта переднего плана из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="b25aa-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="b25aa-109">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет шлюз в $AppGw переменной.</span><span class="sxs-lookup"><span data-stu-id="b25aa-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>

<span data-ttu-id="b25aa-110">Вторая команда удаляет порт с именем FrontEndPort02 из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b25aa-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="b25aa-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b25aa-111">PARAMETERS</span></span>

### <span data-ttu-id="b25aa-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b25aa-112">-ApplicationGateway</span></span>
<span data-ttu-id="b25aa-113">Указывает шлюз приложения, из которого нужно удалить порт переднего плана.</span><span class="sxs-lookup"><span data-stu-id="b25aa-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="b25aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b25aa-114">-DefaultProfile</span></span>
<span data-ttu-id="b25aa-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b25aa-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b25aa-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b25aa-116">-Name</span></span>
<span data-ttu-id="b25aa-117">Указывает имя удаляемого порта переднего плана.</span><span class="sxs-lookup"><span data-stu-id="b25aa-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="b25aa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b25aa-118">CommonParameters</span></span>
<span data-ttu-id="b25aa-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b25aa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b25aa-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b25aa-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b25aa-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b25aa-121">INPUTS</span></span>

### <span data-ttu-id="b25aa-122">System. String</span><span class="sxs-lookup"><span data-stu-id="b25aa-122">System.String</span></span>

## <span data-ttu-id="b25aa-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b25aa-123">OUTPUTS</span></span>

### <span data-ttu-id="b25aa-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b25aa-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b25aa-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="b25aa-125">NOTES</span></span>

## <span data-ttu-id="b25aa-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b25aa-126">RELATED LINKS</span></span>

[<span data-ttu-id="b25aa-127">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b25aa-127">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b25aa-128">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b25aa-128">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b25aa-129">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b25aa-129">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b25aa-130">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b25aa-130">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


