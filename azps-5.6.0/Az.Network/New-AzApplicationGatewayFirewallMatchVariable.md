---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: 824c1c4e98fca6b6f7d2ff3df9217cb000eeaf21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015064"
---
# <span data-ttu-id="b0635-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="b0635-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="b0635-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0635-102">SYNOPSIS</span></span>
<span data-ttu-id="b0635-103">Создает переменную совпадения для условия брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="b0635-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="b0635-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b0635-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0635-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0635-105">DESCRIPTION</span></span>
<span data-ttu-id="b0635-106">Параметр **New-AzApplicationGatewayFirewallMatchVariable** создает переменную совпадения для условия брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="b0635-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="b0635-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b0635-107">EXAMPLES</span></span>

### <span data-ttu-id="b0635-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b0635-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="b0635-109">Команда создает новую переменную совпадения с именем заглавных полей запроса, а селектор — полем "Длина содержимого".</span><span class="sxs-lookup"><span data-stu-id="b0635-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="b0635-110">Новая переменная совпадения будет сохранена в $variable.</span><span class="sxs-lookup"><span data-stu-id="b0635-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="b0635-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0635-111">PARAMETERS</span></span>

### <span data-ttu-id="b0635-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0635-112">-DefaultProfile</span></span>
<span data-ttu-id="b0635-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0635-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0635-114">-Selector</span><span class="sxs-lookup"><span data-stu-id="b0635-114">-Selector</span></span>
<span data-ttu-id="b0635-115">Описание поля matchVariable collection.</span><span class="sxs-lookup"><span data-stu-id="b0635-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="b0635-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="b0635-116">-VariableName</span></span>
<span data-ttu-id="b0635-117">Переменная match.</span><span class="sxs-lookup"><span data-stu-id="b0635-117">Match Variable.</span></span>

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

### <span data-ttu-id="b0635-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0635-118">CommonParameters</span></span>
<span data-ttu-id="b0635-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0635-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0635-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0635-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0635-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0635-121">INPUTS</span></span>

### <span data-ttu-id="b0635-122">Нет</span><span class="sxs-lookup"><span data-stu-id="b0635-122">None</span></span>

## <span data-ttu-id="b0635-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b0635-123">OUTPUTS</span></span>

### <span data-ttu-id="b0635-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="b0635-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="b0635-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b0635-125">NOTES</span></span>

## <span data-ttu-id="b0635-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0635-126">RELATED LINKS</span></span>
