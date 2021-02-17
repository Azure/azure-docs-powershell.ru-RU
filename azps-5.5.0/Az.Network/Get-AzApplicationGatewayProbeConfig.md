---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: ec20d7caafe110f03e5a0ce3130247ec877d6af9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213961"
---
# <span data-ttu-id="3c9f9-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3c9f9-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="3c9f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c9f9-102">SYNOPSIS</span></span>
<span data-ttu-id="3c9f9-103">Получает существующую конфигурацию из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3c9f9-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="3c9f9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3c9f9-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c9f9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c9f9-105">DESCRIPTION</span></span>
<span data-ttu-id="3c9f9-106">Этот Get-AzApplicationGatewayProbeConfig получает существующую конфигурацию из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3c9f9-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="3c9f9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3c9f9-107">EXAMPLES</span></span>

### <span data-ttu-id="3c9f9-108">Пример 1. Получение существующего зака в шлюзе приложения</span><span class="sxs-lookup"><span data-stu-id="3c9f9-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="3c9f9-109">Эта команда получает имя "Проект02" из шлюза приложения "Шлюз".</span><span class="sxs-lookup"><span data-stu-id="3c9f9-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="3c9f9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c9f9-110">PARAMETERS</span></span>

### <span data-ttu-id="3c9f9-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c9f9-111">-ApplicationGateway</span></span>
<span data-ttu-id="3c9f9-112">Указывает шлюз приложения, к которому этот cmdlet получает конфигурацию формы.</span><span class="sxs-lookup"><span data-stu-id="3c9f9-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="3c9f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c9f9-113">-DefaultProfile</span></span>
<span data-ttu-id="3c9f9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c9f9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c9f9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3c9f9-115">-Name</span></span>
<span data-ttu-id="3c9f9-116">Указывает имя вехи.</span><span class="sxs-lookup"><span data-stu-id="3c9f9-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="3c9f9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c9f9-117">CommonParameters</span></span>
<span data-ttu-id="3c9f9-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c9f9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c9f9-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c9f9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c9f9-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c9f9-120">INPUTS</span></span>

### <span data-ttu-id="3c9f9-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c9f9-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3c9f9-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3c9f9-122">OUTPUTS</span></span>

### <span data-ttu-id="3c9f9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="3c9f9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="3c9f9-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3c9f9-124">NOTES</span></span>

## <span data-ttu-id="3c9f9-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c9f9-125">RELATED LINKS</span></span>

[<span data-ttu-id="3c9f9-126">Добавление астройки к существующему шлюзу приложения</span><span class="sxs-lookup"><span data-stu-id="3c9f9-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="3c9f9-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3c9f9-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="3c9f9-128">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3c9f9-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="3c9f9-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3c9f9-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="3c9f9-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3c9f9-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

