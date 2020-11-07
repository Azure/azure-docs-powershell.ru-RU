---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 41693da553178bdd45d19da498a5774ef8d2fa60
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909753"
---
# <span data-ttu-id="a34f9-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="a34f9-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="a34f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a34f9-102">SYNOPSIS</span></span>
<span data-ttu-id="a34f9-103">Создание ответа на запрос проверки работоспособности, который используется зондом проверки работоспособности для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="a34f9-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="a34f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a34f9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a34f9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a34f9-105">DESCRIPTION</span></span>
<span data-ttu-id="a34f9-106">Командлет **Add-AzApplicationGatewayProbeHealthResponseMatch** создает ответ на проверку работоспособности, который используется зондом проверки работоспособности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="a34f9-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="a34f9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a34f9-107">EXAMPLES</span></span>

### <span data-ttu-id="a34f9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a34f9-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="a34f9-109">Эта команда создает ответ на запрос о работоспособности, который можно передать в ProbeConfig в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="a34f9-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="a34f9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a34f9-110">PARAMETERS</span></span>

### <span data-ttu-id="a34f9-111">-Body</span><span class="sxs-lookup"><span data-stu-id="a34f9-111">-Body</span></span>
<span data-ttu-id="a34f9-112">Текст, который должен содержаться в ответе работоспособности.</span><span class="sxs-lookup"><span data-stu-id="a34f9-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="a34f9-113">Пустое значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a34f9-113">Default value is empty</span></span>

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

### <span data-ttu-id="a34f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a34f9-114">-DefaultProfile</span></span>
<span data-ttu-id="a34f9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a34f9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a34f9-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="a34f9-116">-StatusCode</span></span>
<span data-ttu-id="a34f9-117">Допустимые диапазоны работоспособных кодов состояния. Диапазон работоспособных кодов состояния по умолчанию составляет 200-399</span><span class="sxs-lookup"><span data-stu-id="a34f9-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a34f9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a34f9-118">CommonParameters</span></span>
<span data-ttu-id="a34f9-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a34f9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a34f9-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a34f9-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a34f9-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a34f9-121">INPUTS</span></span>

### <span data-ttu-id="a34f9-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="a34f9-122">None</span></span>

## <span data-ttu-id="a34f9-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a34f9-123">OUTPUTS</span></span>

### <span data-ttu-id="a34f9-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="a34f9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="a34f9-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="a34f9-125">NOTES</span></span>

## <span data-ttu-id="a34f9-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a34f9-126">RELATED LINKS</span></span>

