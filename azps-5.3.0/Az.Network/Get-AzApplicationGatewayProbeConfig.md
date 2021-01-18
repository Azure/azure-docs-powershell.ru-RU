---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: ec20d7caafe110f03e5a0ce3130247ec877d6af9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506523"
---
# <span data-ttu-id="e6d89-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e6d89-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="e6d89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6d89-102">SYNOPSIS</span></span>
<span data-ttu-id="e6d89-103">Получает существующую конфигурацию из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e6d89-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="e6d89-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e6d89-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6d89-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6d89-105">DESCRIPTION</span></span>
<span data-ttu-id="e6d89-106">Этот Get-AzApplicationGatewayProbeConfig получает существующую конфигурацию из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e6d89-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="e6d89-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e6d89-107">EXAMPLES</span></span>

### <span data-ttu-id="e6d89-108">Пример 1. Получение существующего зака в шлюзе приложения</span><span class="sxs-lookup"><span data-stu-id="e6d89-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="e6d89-109">Эта команда получает имя "Проект02" из шлюза приложения "Шлюз".</span><span class="sxs-lookup"><span data-stu-id="e6d89-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="e6d89-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6d89-110">PARAMETERS</span></span>

### <span data-ttu-id="e6d89-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6d89-111">-ApplicationGateway</span></span>
<span data-ttu-id="e6d89-112">Указывает шлюз приложения, к которому этот cmdlet получает конфигурацию формы.</span><span class="sxs-lookup"><span data-stu-id="e6d89-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="e6d89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6d89-113">-DefaultProfile</span></span>
<span data-ttu-id="e6d89-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6d89-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6d89-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e6d89-115">-Name</span></span>
<span data-ttu-id="e6d89-116">Указывает имя заме желтого.</span><span class="sxs-lookup"><span data-stu-id="e6d89-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="e6d89-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6d89-117">CommonParameters</span></span>
<span data-ttu-id="e6d89-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6d89-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6d89-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6d89-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6d89-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6d89-120">INPUTS</span></span>

### <span data-ttu-id="e6d89-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6d89-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e6d89-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e6d89-122">OUTPUTS</span></span>

### <span data-ttu-id="e6d89-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="e6d89-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="e6d89-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e6d89-124">NOTES</span></span>

## <span data-ttu-id="e6d89-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6d89-125">RELATED LINKS</span></span>

[<span data-ttu-id="e6d89-126">Добавление астройки к существующему шлюзу приложения</span><span class="sxs-lookup"><span data-stu-id="e6d89-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="e6d89-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e6d89-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="e6d89-128">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e6d89-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="e6d89-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e6d89-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="e6d89-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e6d89-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

