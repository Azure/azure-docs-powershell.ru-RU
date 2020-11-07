---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: cbe38933cb4c2c75b5219bf0deccc0b28052a61f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913835"
---
# <span data-ttu-id="d28f7-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d28f7-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="d28f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d28f7-102">SYNOPSIS</span></span>
<span data-ttu-id="d28f7-103">Получает существующую конфигурацию проверки работоспособности из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="d28f7-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d28f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d28f7-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d28f7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d28f7-105">DESCRIPTION</span></span>
<span data-ttu-id="d28f7-106">Командлет Get-AzureRmApplicationGatewayProbeConfig получает существующую конфигурацию проверки работоспособности из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="d28f7-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="d28f7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d28f7-107">EXAMPLES</span></span>

### <span data-ttu-id="d28f7-108">Пример 1: получение существующего пробного зонда из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="d28f7-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="d28f7-109">Эта команда получает проверку работоспособности с именем Probe02 из шлюза приложений с именем Gateway.</span><span class="sxs-lookup"><span data-stu-id="d28f7-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="d28f7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d28f7-110">PARAMETERS</span></span>

### <span data-ttu-id="d28f7-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d28f7-111">-ApplicationGateway</span></span>
<span data-ttu-id="d28f7-112">Указывает шлюз приложений, которому этот командлет получает конфигурацию зонда.</span><span class="sxs-lookup"><span data-stu-id="d28f7-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="d28f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d28f7-113">-DefaultProfile</span></span>
<span data-ttu-id="d28f7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d28f7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d28f7-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d28f7-115">-Name</span></span>
<span data-ttu-id="d28f7-116">Указывает имя зонда.</span><span class="sxs-lookup"><span data-stu-id="d28f7-116">Specifies the name of the probe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d28f7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d28f7-117">CommonParameters</span></span>
<span data-ttu-id="d28f7-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d28f7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d28f7-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d28f7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d28f7-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d28f7-120">INPUTS</span></span>

### <span data-ttu-id="d28f7-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d28f7-121">PSApplicationGateway</span></span>
<span data-ttu-id="d28f7-122">Параметр "ApplicationGateway" принимает значение типа "PSApplicationGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d28f7-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="d28f7-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d28f7-123">OUTPUTS</span></span>

### <span data-ttu-id="d28f7-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="d28f7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="d28f7-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Networking. Models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="d28f7-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="d28f7-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="d28f7-126">NOTES</span></span>

## <span data-ttu-id="d28f7-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d28f7-127">RELATED LINKS</span></span>

[<span data-ttu-id="d28f7-128">Добавление зонда к существующему шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="d28f7-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="d28f7-129">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d28f7-129">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="d28f7-130">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d28f7-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="d28f7-131">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d28f7-131">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="d28f7-132">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d28f7-132">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

