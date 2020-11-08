---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 20704f404d5fe47267f42398ef885fb2c038f84e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245970"
---
# <span data-ttu-id="b8f42-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b8f42-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="b8f42-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8f42-102">SYNOPSIS</span></span>
<span data-ttu-id="b8f42-103">Удаление проверки работоспособности из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b8f42-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="b8f42-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8f42-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8f42-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8f42-105">DESCRIPTION</span></span>
<span data-ttu-id="b8f42-106">Командлет Remove-AzApplicationGatewayProbeConfig удаляет проверку работоспособности из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b8f42-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="b8f42-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8f42-107">EXAMPLES</span></span>

### <span data-ttu-id="b8f42-108">Пример 1: Удаление проверки работоспособности из существующего шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="b8f42-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="b8f42-109">Эта команда удаляет проверку работоспособности с именем Probe04 из шлюза приложений с именем Gateway.</span><span class="sxs-lookup"><span data-stu-id="b8f42-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="b8f42-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8f42-110">PARAMETERS</span></span>

### <span data-ttu-id="b8f42-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8f42-111">-ApplicationGateway</span></span>
<span data-ttu-id="b8f42-112">Указывает шлюз приложений, с которым этот командлет удаляет зонд.</span><span class="sxs-lookup"><span data-stu-id="b8f42-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="b8f42-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8f42-113">-DefaultProfile</span></span>
<span data-ttu-id="b8f42-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8f42-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8f42-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8f42-115">-Name</span></span>
<span data-ttu-id="b8f42-116">Указывает имя пробной версии, для которого удаляется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b8f42-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="b8f42-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8f42-117">CommonParameters</span></span>
<span data-ttu-id="b8f42-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8f42-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8f42-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8f42-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8f42-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8f42-120">INPUTS</span></span>

### <span data-ttu-id="b8f42-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8f42-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b8f42-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8f42-122">OUTPUTS</span></span>

### <span data-ttu-id="b8f42-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8f42-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b8f42-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8f42-124">NOTES</span></span>

## <span data-ttu-id="b8f42-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8f42-125">RELATED LINKS</span></span>

[<span data-ttu-id="b8f42-126">Удаление пробы из существующего шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="b8f42-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="b8f42-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b8f42-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="b8f42-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b8f42-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="b8f42-129">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b8f42-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="b8f42-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b8f42-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

