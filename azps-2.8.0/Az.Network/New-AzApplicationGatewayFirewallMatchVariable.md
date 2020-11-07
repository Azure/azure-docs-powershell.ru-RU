---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: b7d49645426425f914714f65c244974277e975e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902233"
---
# <span data-ttu-id="7ae71-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="7ae71-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="7ae71-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7ae71-102">SYNOPSIS</span></span>
<span data-ttu-id="7ae71-103">Создание переменной соответствия для условия брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="7ae71-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="7ae71-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7ae71-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ae71-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ae71-105">DESCRIPTION</span></span>
<span data-ttu-id="7ae71-106">**New-AzApplicationGatewayFirewallMatchVariable** создает переменную Match для условия межсетевого экрана.</span><span class="sxs-lookup"><span data-stu-id="7ae71-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="7ae71-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7ae71-107">EXAMPLES</span></span>

### <span data-ttu-id="7ae71-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7ae71-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="7ae71-109">Команда создает новую переменную Match с именем заголовков запроса и Selector — поле Content-Length.</span><span class="sxs-lookup"><span data-stu-id="7ae71-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="7ae71-110">Новая переменная соответствия сохраняется в $variable.</span><span class="sxs-lookup"><span data-stu-id="7ae71-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="7ae71-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7ae71-111">PARAMETERS</span></span>

### <span data-ttu-id="7ae71-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ae71-112">-DefaultProfile</span></span>
<span data-ttu-id="7ae71-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7ae71-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ae71-114">-Selector</span><span class="sxs-lookup"><span data-stu-id="7ae71-114">-Selector</span></span>
<span data-ttu-id="7ae71-115">Описание поля коллекции matchVariable.</span><span class="sxs-lookup"><span data-stu-id="7ae71-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="7ae71-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="7ae71-116">-VariableName</span></span>
<span data-ttu-id="7ae71-117">Переменная Match.</span><span class="sxs-lookup"><span data-stu-id="7ae71-117">Match Variable.</span></span>

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

### <span data-ttu-id="7ae71-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ae71-118">CommonParameters</span></span>
<span data-ttu-id="7ae71-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7ae71-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ae71-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ae71-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ae71-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7ae71-121">INPUTS</span></span>

### <span data-ttu-id="7ae71-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="7ae71-122">None</span></span>

## <span data-ttu-id="7ae71-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ae71-123">OUTPUTS</span></span>

### <span data-ttu-id="7ae71-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="7ae71-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="7ae71-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="7ae71-125">NOTES</span></span>

## <span data-ttu-id="7ae71-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ae71-126">RELATED LINKS</span></span>
