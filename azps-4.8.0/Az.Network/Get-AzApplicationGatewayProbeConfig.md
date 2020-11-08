---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: ec20d7caafe110f03e5a0ce3130247ec877d6af9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236975"
---
# <span data-ttu-id="dc0f4-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dc0f4-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="dc0f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc0f4-102">SYNOPSIS</span></span>
<span data-ttu-id="dc0f4-103">Получает существующую конфигурацию проверки работоспособности из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="dc0f4-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="dc0f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc0f4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc0f4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc0f4-105">DESCRIPTION</span></span>
<span data-ttu-id="dc0f4-106">Командлет Get-AzApplicationGatewayProbeConfig получает существующую конфигурацию проверки работоспособности из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="dc0f4-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="dc0f4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc0f4-107">EXAMPLES</span></span>

### <span data-ttu-id="dc0f4-108">Пример 1: получение существующего пробного зонда из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="dc0f4-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="dc0f4-109">Эта команда получает проверку работоспособности с именем Probe02 из шлюза приложений с именем Gateway.</span><span class="sxs-lookup"><span data-stu-id="dc0f4-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="dc0f4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc0f4-110">PARAMETERS</span></span>

### <span data-ttu-id="dc0f4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc0f4-111">-ApplicationGateway</span></span>
<span data-ttu-id="dc0f4-112">Указывает шлюз приложений, которому этот командлет получает конфигурацию зонда.</span><span class="sxs-lookup"><span data-stu-id="dc0f4-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="dc0f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc0f4-113">-DefaultProfile</span></span>
<span data-ttu-id="dc0f4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc0f4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc0f4-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc0f4-115">-Name</span></span>
<span data-ttu-id="dc0f4-116">Указывает имя зонда.</span><span class="sxs-lookup"><span data-stu-id="dc0f4-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="dc0f4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc0f4-117">CommonParameters</span></span>
<span data-ttu-id="dc0f4-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc0f4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc0f4-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc0f4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc0f4-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc0f4-120">INPUTS</span></span>

### <span data-ttu-id="dc0f4-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc0f4-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dc0f4-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc0f4-122">OUTPUTS</span></span>

### <span data-ttu-id="dc0f4-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="dc0f4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="dc0f4-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc0f4-124">NOTES</span></span>

## <span data-ttu-id="dc0f4-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc0f4-125">RELATED LINKS</span></span>

[<span data-ttu-id="dc0f4-126">Добавление зонда к существующему шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="dc0f4-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="dc0f4-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dc0f4-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="dc0f4-128">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dc0f4-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="dc0f4-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dc0f4-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="dc0f4-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dc0f4-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

