---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: c3ff96a2c1d06fdfba5879244b058ef1a7845f40
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234995"
---
# <span data-ttu-id="e8430-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="e8430-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="e8430-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8430-102">SYNOPSIS</span></span>
<span data-ttu-id="e8430-103">Создание переменной соответствия для условия брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="e8430-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="e8430-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8430-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8430-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8430-105">DESCRIPTION</span></span>
<span data-ttu-id="e8430-106">**New-AzApplicationGatewayFirewallMatchVariable** создает переменную Match для условия межсетевого экрана.</span><span class="sxs-lookup"><span data-stu-id="e8430-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="e8430-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8430-107">EXAMPLES</span></span>

### <span data-ttu-id="e8430-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e8430-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="e8430-109">Команда создает новую переменную Match с именем заголовков запроса и Selector — поле Content-Length.</span><span class="sxs-lookup"><span data-stu-id="e8430-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="e8430-110">Новая переменная соответствия сохраняется в $variable.</span><span class="sxs-lookup"><span data-stu-id="e8430-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="e8430-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8430-111">PARAMETERS</span></span>

### <span data-ttu-id="e8430-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8430-112">-DefaultProfile</span></span>
<span data-ttu-id="e8430-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8430-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8430-114">-Selector</span><span class="sxs-lookup"><span data-stu-id="e8430-114">-Selector</span></span>
<span data-ttu-id="e8430-115">Описание поля коллекции matchVariable.</span><span class="sxs-lookup"><span data-stu-id="e8430-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="e8430-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="e8430-116">-VariableName</span></span>
<span data-ttu-id="e8430-117">Переменная Match.</span><span class="sxs-lookup"><span data-stu-id="e8430-117">Match Variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeaders, RequestBody, RequestCookies

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8430-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8430-118">CommonParameters</span></span>
<span data-ttu-id="e8430-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8430-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8430-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8430-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8430-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8430-121">INPUTS</span></span>

### <span data-ttu-id="e8430-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="e8430-122">None</span></span>

## <span data-ttu-id="e8430-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8430-123">OUTPUTS</span></span>

### <span data-ttu-id="e8430-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="e8430-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="e8430-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8430-125">NOTES</span></span>

## <span data-ttu-id="e8430-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8430-126">RELATED LINKS</span></span>
