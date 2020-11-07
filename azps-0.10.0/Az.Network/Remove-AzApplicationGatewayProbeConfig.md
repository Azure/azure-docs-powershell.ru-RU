---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 320588b81791c033b94a07261f769fa0886d2f2c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909545"
---
# <span data-ttu-id="a0f1a-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a0f1a-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="a0f1a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a0f1a-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f1a-103">Удаление проверки работоспособности из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="a0f1a-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="a0f1a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a0f1a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0f1a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0f1a-105">DESCRIPTION</span></span>
<span data-ttu-id="a0f1a-106">Командлет Remove-AzApplicationGatewayProbeConfig удаляет проверку работоспособности из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="a0f1a-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="a0f1a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a0f1a-107">EXAMPLES</span></span>

### <span data-ttu-id="a0f1a-108">Пример 1: Удаление проверки работоспособности из существующего шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="a0f1a-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="a0f1a-109">Эта команда удаляет проверку работоспособности с именем Probe04 из шлюза приложений с именем Gateway.</span><span class="sxs-lookup"><span data-stu-id="a0f1a-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="a0f1a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a0f1a-110">PARAMETERS</span></span>

### <span data-ttu-id="a0f1a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0f1a-111">-ApplicationGateway</span></span>
<span data-ttu-id="a0f1a-112">Указывает шлюз приложений, с которым этот командлет удаляет зонд.</span><span class="sxs-lookup"><span data-stu-id="a0f1a-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="a0f1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f1a-113">-DefaultProfile</span></span>
<span data-ttu-id="a0f1a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0f1a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0f1a-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a0f1a-115">-Name</span></span>
<span data-ttu-id="a0f1a-116">Указывает имя пробной версии, для которого удаляется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a0f1a-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f1a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f1a-117">CommonParameters</span></span>
<span data-ttu-id="a0f1a-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a0f1a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f1a-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0f1a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f1a-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a0f1a-120">INPUTS</span></span>

### <span data-ttu-id="a0f1a-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0f1a-121">PSApplicationGateway</span></span>
<span data-ttu-id="a0f1a-122">Параметр "ApplicationGateway" принимает значение типа "PSApplicationGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a0f1a-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="a0f1a-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0f1a-123">OUTPUTS</span></span>

### <span data-ttu-id="a0f1a-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0f1a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a0f1a-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="a0f1a-125">NOTES</span></span>

## <span data-ttu-id="a0f1a-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0f1a-126">RELATED LINKS</span></span>

[<span data-ttu-id="a0f1a-127">Удаление пробы из существующего шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="a0f1a-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="a0f1a-128">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a0f1a-128">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="a0f1a-129">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a0f1a-129">Get-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="a0f1a-130">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a0f1a-130">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="a0f1a-131">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a0f1a-131">Set-AzApplicationGatewayProbeConfig</span></span>]()

