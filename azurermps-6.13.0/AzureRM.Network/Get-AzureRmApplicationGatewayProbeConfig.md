---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 2730e3ba1e85a876940492b4abfd4fbe5dbca956
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567279"
---
# <span data-ttu-id="01804-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="01804-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="01804-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01804-102">SYNOPSIS</span></span>
<span data-ttu-id="01804-103">Получает существующую конфигурацию проверки работоспособности из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="01804-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01804-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01804-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01804-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01804-105">DESCRIPTION</span></span>
<span data-ttu-id="01804-106">Командлет Get-AzureRmApplicationGatewayProbeConfig получает существующую конфигурацию проверки работоспособности из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="01804-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="01804-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01804-107">EXAMPLES</span></span>

### <span data-ttu-id="01804-108">Пример 1: получение существующего пробного зонда из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="01804-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="01804-109">Эта команда получает проверку работоспособности с именем Probe02 из шлюза приложений с именем Gateway.</span><span class="sxs-lookup"><span data-stu-id="01804-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="01804-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01804-110">PARAMETERS</span></span>

### <span data-ttu-id="01804-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01804-111">-ApplicationGateway</span></span>
<span data-ttu-id="01804-112">Указывает шлюз приложений, которому этот командлет получает конфигурацию зонда.</span><span class="sxs-lookup"><span data-stu-id="01804-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="01804-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01804-113">-DefaultProfile</span></span>
<span data-ttu-id="01804-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01804-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01804-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="01804-115">-Name</span></span>
<span data-ttu-id="01804-116">Указывает имя зонда.</span><span class="sxs-lookup"><span data-stu-id="01804-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="01804-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01804-117">CommonParameters</span></span>
<span data-ttu-id="01804-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01804-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01804-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01804-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01804-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01804-120">INPUTS</span></span>

### <span data-ttu-id="01804-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01804-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="01804-122">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="01804-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="01804-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01804-123">OUTPUTS</span></span>

### <span data-ttu-id="01804-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="01804-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="01804-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="01804-125">NOTES</span></span>

## <span data-ttu-id="01804-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01804-126">RELATED LINKS</span></span>

[<span data-ttu-id="01804-127">Добавление зонда к существующему шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="01804-127">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="01804-128">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="01804-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="01804-129">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="01804-129">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="01804-130">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="01804-130">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="01804-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="01804-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

