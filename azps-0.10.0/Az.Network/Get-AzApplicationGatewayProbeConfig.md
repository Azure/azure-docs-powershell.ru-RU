---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: b3e2b3ea03ca0bae0db1bea1606e4ae6b94a597e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910070"
---
# <span data-ttu-id="81d33-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="81d33-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="81d33-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81d33-102">SYNOPSIS</span></span>
<span data-ttu-id="81d33-103">Получает существующую конфигурацию проверки работоспособности из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="81d33-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="81d33-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81d33-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81d33-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81d33-105">DESCRIPTION</span></span>
<span data-ttu-id="81d33-106">Командлет Get-AzApplicationGatewayProbeConfig получает существующую конфигурацию проверки работоспособности из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="81d33-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="81d33-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81d33-107">EXAMPLES</span></span>

### <span data-ttu-id="81d33-108">Пример 1: получение существующего пробного зонда из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="81d33-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="81d33-109">Эта команда получает проверку работоспособности с именем Probe02 из шлюза приложений с именем Gateway.</span><span class="sxs-lookup"><span data-stu-id="81d33-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="81d33-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81d33-110">PARAMETERS</span></span>

### <span data-ttu-id="81d33-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81d33-111">-ApplicationGateway</span></span>
<span data-ttu-id="81d33-112">Указывает шлюз приложений, которому этот командлет получает конфигурацию зонда.</span><span class="sxs-lookup"><span data-stu-id="81d33-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="81d33-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d33-113">-DefaultProfile</span></span>
<span data-ttu-id="81d33-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81d33-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81d33-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="81d33-115">-Name</span></span>
<span data-ttu-id="81d33-116">Указывает имя зонда.</span><span class="sxs-lookup"><span data-stu-id="81d33-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="81d33-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d33-117">CommonParameters</span></span>
<span data-ttu-id="81d33-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81d33-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d33-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81d33-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d33-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81d33-120">INPUTS</span></span>

### <span data-ttu-id="81d33-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81d33-121">PSApplicationGateway</span></span>
<span data-ttu-id="81d33-122">Параметр "ApplicationGateway" принимает значение типа "PSApplicationGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="81d33-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="81d33-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81d33-123">OUTPUTS</span></span>

### <span data-ttu-id="81d33-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="81d33-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="81d33-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Networking. Models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="81d33-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="81d33-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="81d33-126">NOTES</span></span>

## <span data-ttu-id="81d33-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81d33-127">RELATED LINKS</span></span>

[<span data-ttu-id="81d33-128">Добавление зонда к существующему шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="81d33-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="81d33-129">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="81d33-129">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="81d33-130">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="81d33-130">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="81d33-131">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="81d33-131">Remove-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="81d33-132">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="81d33-132">Set-AzApplicationGatewayProbeConfig</span></span>]()

