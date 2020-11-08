---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: edc0309b5e1a0c8b17d400e965074d38ca02bb80
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248564"
---
# <span data-ttu-id="1fc47-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="1fc47-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="1fc47-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1fc47-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc47-103">Создание ответа на запрос проверки работоспособности, который используется зондом проверки работоспособности для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1fc47-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="1fc47-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1fc47-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fc47-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fc47-105">DESCRIPTION</span></span>
<span data-ttu-id="1fc47-106">Командлет **Add-AzApplicationGatewayProbeHealthResponseMatch** создает ответ на проверку работоспособности, который используется зондом проверки работоспособности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="1fc47-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="1fc47-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1fc47-107">EXAMPLES</span></span>

### <span data-ttu-id="1fc47-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1fc47-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="1fc47-109">Эта команда создает ответ на запрос о работоспособности, который можно передать в ProbeConfig в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="1fc47-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="1fc47-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1fc47-110">PARAMETERS</span></span>

### <span data-ttu-id="1fc47-111">-Body</span><span class="sxs-lookup"><span data-stu-id="1fc47-111">-Body</span></span>
<span data-ttu-id="1fc47-112">Текст, который должен содержаться в ответе работоспособности.</span><span class="sxs-lookup"><span data-stu-id="1fc47-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="1fc47-113">Пустое значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1fc47-113">Default value is empty</span></span>

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

### <span data-ttu-id="1fc47-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fc47-114">-DefaultProfile</span></span>
<span data-ttu-id="1fc47-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fc47-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fc47-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="1fc47-116">-StatusCode</span></span>
<span data-ttu-id="1fc47-117">Допустимые диапазоны работоспособных кодов состояния. Диапазон работоспособных кодов состояния по умолчанию составляет 200-399</span><span class="sxs-lookup"><span data-stu-id="1fc47-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc47-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc47-118">CommonParameters</span></span>
<span data-ttu-id="1fc47-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1fc47-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc47-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fc47-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc47-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1fc47-121">INPUTS</span></span>

### <span data-ttu-id="1fc47-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="1fc47-122">None</span></span>

## <span data-ttu-id="1fc47-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fc47-123">OUTPUTS</span></span>

### <span data-ttu-id="1fc47-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="1fc47-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="1fc47-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="1fc47-125">NOTES</span></span>

## <span data-ttu-id="1fc47-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fc47-126">RELATED LINKS</span></span>
