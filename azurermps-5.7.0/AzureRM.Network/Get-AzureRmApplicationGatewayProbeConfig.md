---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: d8086718ef9d4b009bc785a3017c38e8d29047c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564795"
---
# <span data-ttu-id="dafcf-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dafcf-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="dafcf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dafcf-102">SYNOPSIS</span></span>
<span data-ttu-id="dafcf-103">Получает существующую конфигурацию проверки работоспособности из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="dafcf-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dafcf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dafcf-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dafcf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dafcf-105">DESCRIPTION</span></span>
<span data-ttu-id="dafcf-106">Командлет Get-AzureRmApplicationGatewayProbeConfig получает существующую конфигурацию проверки работоспособности из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="dafcf-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="dafcf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dafcf-107">EXAMPLES</span></span>

### <span data-ttu-id="dafcf-108">Пример 1: получение существующего пробного зонда из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="dafcf-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="dafcf-109">Эта команда получает проверку работоспособности с именем Probe02 из шлюза приложений с именем Gateway.</span><span class="sxs-lookup"><span data-stu-id="dafcf-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="dafcf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dafcf-110">PARAMETERS</span></span>

### <span data-ttu-id="dafcf-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dafcf-111">-ApplicationGateway</span></span>
<span data-ttu-id="dafcf-112">Указывает шлюз приложений, которому этот командлет получает конфигурацию зонда.</span><span class="sxs-lookup"><span data-stu-id="dafcf-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="dafcf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dafcf-113">-DefaultProfile</span></span>
<span data-ttu-id="dafcf-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dafcf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dafcf-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dafcf-115">-Name</span></span>
<span data-ttu-id="dafcf-116">Указывает имя зонда.</span><span class="sxs-lookup"><span data-stu-id="dafcf-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="dafcf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dafcf-117">CommonParameters</span></span>
<span data-ttu-id="dafcf-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dafcf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dafcf-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dafcf-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dafcf-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dafcf-120">INPUTS</span></span>

### <span data-ttu-id="dafcf-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dafcf-121">PSApplicationGateway</span></span>
<span data-ttu-id="dafcf-122">Параметр "ApplicationGateway" принимает значение типа "PSApplicationGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="dafcf-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="dafcf-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dafcf-123">OUTPUTS</span></span>

### <span data-ttu-id="dafcf-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="dafcf-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="dafcf-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Networking. Models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="dafcf-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="dafcf-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="dafcf-126">NOTES</span></span>

## <span data-ttu-id="dafcf-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dafcf-127">RELATED LINKS</span></span>

[<span data-ttu-id="dafcf-128">Добавление зонда к существующему шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="dafcf-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="dafcf-129">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dafcf-129">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="dafcf-130">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dafcf-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="dafcf-131">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dafcf-131">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="dafcf-132">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dafcf-132">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

