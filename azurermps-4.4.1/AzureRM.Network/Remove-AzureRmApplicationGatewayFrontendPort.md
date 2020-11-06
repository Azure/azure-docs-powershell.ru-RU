---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 9e3a9a515f7b33e23cb7444baa281e083c3c10ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565242"
---
# <span data-ttu-id="8f0e5-101">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8f0e5-101">Remove-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="8f0e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f0e5-102">SYNOPSIS</span></span>
<span data-ttu-id="8f0e5-103">Удаляет интерфейсный порт из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="8f0e5-103">Removes a front-end port from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f0e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f0e5-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f0e5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f0e5-105">DESCRIPTION</span></span>
<span data-ttu-id="8f0e5-106">Командлет **Remove-AzureRmApplicationGatewayFrontendPort** удаляет интерфейсный порт из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="8f0e5-106">The **Remove-AzureRmApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="8f0e5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f0e5-107">EXAMPLES</span></span>

### <span data-ttu-id="8f0e5-108">Пример: Удаление порта переднего плана из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="8f0e5-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="8f0e5-109">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет шлюз в $AppGw переменной.</span><span class="sxs-lookup"><span data-stu-id="8f0e5-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>

<span data-ttu-id="8f0e5-110">Вторая команда удаляет порт с именем FrontEndPort02 из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="8f0e5-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="8f0e5-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f0e5-111">PARAMETERS</span></span>

### <span data-ttu-id="8f0e5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8f0e5-112">-ApplicationGateway</span></span>
<span data-ttu-id="8f0e5-113">Указывает шлюз приложения, из которого нужно удалить порт переднего плана.</span><span class="sxs-lookup"><span data-stu-id="8f0e5-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="8f0e5-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8f0e5-114">-Name</span></span>
<span data-ttu-id="8f0e5-115">Указывает имя удаляемого порта переднего плана.</span><span class="sxs-lookup"><span data-stu-id="8f0e5-115">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="8f0e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f0e5-116">-DefaultProfile</span></span>
<span data-ttu-id="8f0e5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f0e5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f0e5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f0e5-118">CommonParameters</span></span>
<span data-ttu-id="8f0e5-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f0e5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f0e5-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f0e5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f0e5-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f0e5-121">INPUTS</span></span>

### <span data-ttu-id="8f0e5-122">System. String</span><span class="sxs-lookup"><span data-stu-id="8f0e5-122">System.String</span></span>

## <span data-ttu-id="8f0e5-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f0e5-123">OUTPUTS</span></span>

### <span data-ttu-id="8f0e5-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8f0e5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8f0e5-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f0e5-125">NOTES</span></span>

## <span data-ttu-id="8f0e5-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f0e5-126">RELATED LINKS</span></span>

[<span data-ttu-id="8f0e5-127">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8f0e5-127">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="8f0e5-128">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8f0e5-128">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="8f0e5-129">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8f0e5-129">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="8f0e5-130">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8f0e5-130">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


