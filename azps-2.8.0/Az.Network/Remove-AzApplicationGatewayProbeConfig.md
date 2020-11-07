---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: eedb3eb0df28b3f02690a2462b9367995235fcc7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902005"
---
# <span data-ttu-id="ae1f4-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ae1f4-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="ae1f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae1f4-102">SYNOPSIS</span></span>
<span data-ttu-id="ae1f4-103">Удаление проверки работоспособности из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="ae1f4-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="ae1f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae1f4-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae1f4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae1f4-105">DESCRIPTION</span></span>
<span data-ttu-id="ae1f4-106">Командлет Remove-AzApplicationGatewayProbeConfig удаляет проверку работоспособности из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="ae1f4-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="ae1f4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae1f4-107">EXAMPLES</span></span>

### <span data-ttu-id="ae1f4-108">Пример 1: Удаление проверки работоспособности из существующего шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="ae1f4-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="ae1f4-109">Эта команда удаляет проверку работоспособности с именем Probe04 из шлюза приложений с именем Gateway.</span><span class="sxs-lookup"><span data-stu-id="ae1f4-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="ae1f4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae1f4-110">PARAMETERS</span></span>

### <span data-ttu-id="ae1f4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae1f4-111">-ApplicationGateway</span></span>
<span data-ttu-id="ae1f4-112">Указывает шлюз приложений, с которым этот командлет удаляет зонд.</span><span class="sxs-lookup"><span data-stu-id="ae1f4-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="ae1f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae1f4-113">-DefaultProfile</span></span>
<span data-ttu-id="ae1f4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae1f4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae1f4-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ae1f4-115">-Name</span></span>
<span data-ttu-id="ae1f4-116">Указывает имя пробной версии, для которого удаляется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ae1f4-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="ae1f4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae1f4-117">CommonParameters</span></span>
<span data-ttu-id="ae1f4-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae1f4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae1f4-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae1f4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae1f4-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae1f4-120">INPUTS</span></span>

### <span data-ttu-id="ae1f4-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae1f4-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ae1f4-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae1f4-122">OUTPUTS</span></span>

### <span data-ttu-id="ae1f4-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae1f4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ae1f4-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae1f4-124">NOTES</span></span>

## <span data-ttu-id="ae1f4-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae1f4-125">RELATED LINKS</span></span>

[<span data-ttu-id="ae1f4-126">Удаление пробы из существующего шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="ae1f4-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="ae1f4-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ae1f4-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="ae1f4-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ae1f4-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="ae1f4-129">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ae1f4-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="ae1f4-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ae1f4-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

