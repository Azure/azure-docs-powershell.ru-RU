---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 8ee58ee3f6c7a92fac0cb3c92f0a45966e4e875e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991010"
---
# <span data-ttu-id="0c0ce-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0c0ce-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="0c0ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c0ce-102">SYNOPSIS</span></span>
<span data-ttu-id="0c0ce-103">Удаляет заму из существующего шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="0c0ce-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="0c0ce-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0c0ce-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c0ce-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c0ce-105">DESCRIPTION</span></span>
<span data-ttu-id="0c0ce-106">С Remove-AzApplicationGatewayProbeConfig-за него удаляется из существующего шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="0c0ce-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="0c0ce-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0c0ce-107">EXAMPLES</span></span>

### <span data-ttu-id="0c0ce-108">Пример 1. Удаление из существующего шлюза приложения из области "Состояние здоровья"</span><span class="sxs-lookup"><span data-stu-id="0c0ce-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="0c0ce-109">Эта команда удаляет из шлюза приложения "Шлюз" службу состояния с именем "Проект04".</span><span class="sxs-lookup"><span data-stu-id="0c0ce-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="0c0ce-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c0ce-110">PARAMETERS</span></span>

### <span data-ttu-id="0c0ce-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c0ce-111">-ApplicationGateway</span></span>
<span data-ttu-id="0c0ce-112">Указывает шлюз приложения, для которого этот cmdlet удаляет замещает.</span><span class="sxs-lookup"><span data-stu-id="0c0ce-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="0c0ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c0ce-113">-DefaultProfile</span></span>
<span data-ttu-id="0c0ce-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c0ce-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c0ce-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0c0ce-115">-Name</span></span>
<span data-ttu-id="0c0ce-116">Указывает имя фамилии, для которой этот cmdlet удаляет.</span><span class="sxs-lookup"><span data-stu-id="0c0ce-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="0c0ce-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c0ce-117">CommonParameters</span></span>
<span data-ttu-id="0c0ce-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c0ce-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c0ce-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c0ce-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c0ce-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c0ce-120">INPUTS</span></span>

### <span data-ttu-id="0c0ce-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c0ce-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0c0ce-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0c0ce-122">OUTPUTS</span></span>

### <span data-ttu-id="0c0ce-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c0ce-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0c0ce-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0c0ce-124">NOTES</span></span>

## <span data-ttu-id="0c0ce-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c0ce-125">RELATED LINKS</span></span>

[<span data-ttu-id="0c0ce-126">Удаление из существующего шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="0c0ce-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="0c0ce-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0c0ce-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="0c0ce-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0c0ce-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="0c0ce-129">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0c0ce-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="0c0ce-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0c0ce-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

