---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 04da18bcd50fa547f1a59142682c93b4e3e5ab62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974787"
---
# <span data-ttu-id="657f9-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="657f9-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="657f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="657f9-102">SYNOPSIS</span></span>
<span data-ttu-id="657f9-103">Создание совпадения с ответом на проблемы здоровья, используемой в Качестве альтернативы для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="657f9-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="657f9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="657f9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="657f9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="657f9-105">DESCRIPTION</span></span>
<span data-ttu-id="657f9-106">**Командлет Add-AzApplicationGatewayProbeHealthResponseMatch** создает ответ в области здоровья, используемый в Качестве альтернативы для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="657f9-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="657f9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="657f9-107">EXAMPLES</span></span>

### <span data-ttu-id="657f9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="657f9-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="657f9-109">Эта команда создает соответствие ответов на состояние, которое можно передать в Качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="657f9-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="657f9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="657f9-110">PARAMETERS</span></span>

### <span data-ttu-id="657f9-111">-Body</span><span class="sxs-lookup"><span data-stu-id="657f9-111">-Body</span></span>
<span data-ttu-id="657f9-112">Body that must be contained in the health response.</span><span class="sxs-lookup"><span data-stu-id="657f9-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="657f9-113">Значение по умолчанию пустое</span><span class="sxs-lookup"><span data-stu-id="657f9-113">Default value is empty</span></span>

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

### <span data-ttu-id="657f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="657f9-114">-DefaultProfile</span></span>
<span data-ttu-id="657f9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="657f9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="657f9-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="657f9-116">-StatusCode</span></span>
<span data-ttu-id="657f9-117">Допустимые диапазоны кодов состояния. Диапазон здорового состояния по умолчанию составляет 200–399</span><span class="sxs-lookup"><span data-stu-id="657f9-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="657f9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="657f9-118">CommonParameters</span></span>
<span data-ttu-id="657f9-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="657f9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="657f9-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="657f9-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="657f9-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="657f9-121">INPUTS</span></span>

### <span data-ttu-id="657f9-122">Нет</span><span class="sxs-lookup"><span data-stu-id="657f9-122">None</span></span>

## <span data-ttu-id="657f9-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="657f9-123">OUTPUTS</span></span>

### <span data-ttu-id="657f9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="657f9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="657f9-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="657f9-125">NOTES</span></span>

## <span data-ttu-id="657f9-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="657f9-126">RELATED LINKS</span></span>
