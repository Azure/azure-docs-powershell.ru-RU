---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 20704f404d5fe47267f42398ef885fb2c038f84e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064819"
---
# <span data-ttu-id="89eea-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="89eea-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="89eea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89eea-102">SYNOPSIS</span></span>
<span data-ttu-id="89eea-103">Удаление проверки работоспособности из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="89eea-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="89eea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89eea-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89eea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89eea-105">DESCRIPTION</span></span>
<span data-ttu-id="89eea-106">Командлет Remove-AzApplicationGatewayProbeConfig удаляет проверку работоспособности из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="89eea-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="89eea-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89eea-107">EXAMPLES</span></span>

### <span data-ttu-id="89eea-108">Пример 1: Удаление проверки работоспособности из существующего шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="89eea-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="89eea-109">Эта команда удаляет проверку работоспособности с именем Probe04 из шлюза приложений с именем Gateway.</span><span class="sxs-lookup"><span data-stu-id="89eea-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="89eea-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89eea-110">PARAMETERS</span></span>

### <span data-ttu-id="89eea-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89eea-111">-ApplicationGateway</span></span>
<span data-ttu-id="89eea-112">Указывает шлюз приложений, с которым этот командлет удаляет зонд.</span><span class="sxs-lookup"><span data-stu-id="89eea-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="89eea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89eea-113">-DefaultProfile</span></span>
<span data-ttu-id="89eea-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89eea-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89eea-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="89eea-115">-Name</span></span>
<span data-ttu-id="89eea-116">Указывает имя пробной версии, для которого удаляется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="89eea-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="89eea-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89eea-117">CommonParameters</span></span>
<span data-ttu-id="89eea-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89eea-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89eea-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89eea-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89eea-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89eea-120">INPUTS</span></span>

### <span data-ttu-id="89eea-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89eea-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="89eea-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89eea-122">OUTPUTS</span></span>

### <span data-ttu-id="89eea-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89eea-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="89eea-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="89eea-124">NOTES</span></span>

## <span data-ttu-id="89eea-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89eea-125">RELATED LINKS</span></span>

[<span data-ttu-id="89eea-126">Удаление пробы из существующего шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="89eea-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="89eea-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="89eea-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="89eea-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="89eea-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="89eea-129">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="89eea-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="89eea-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="89eea-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

