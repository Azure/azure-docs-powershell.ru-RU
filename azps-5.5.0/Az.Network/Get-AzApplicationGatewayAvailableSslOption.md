---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: f2175583aaaf3af04120e22e32db79d7b20f1e30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223948"
---
# <span data-ttu-id="8b250-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="8b250-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="8b250-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b250-102">SYNOPSIS</span></span>
<span data-ttu-id="8b250-103">Все доступные параметры ssl для SSL-политики для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="8b250-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="8b250-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8b250-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b250-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b250-105">DESCRIPTION</span></span>
<span data-ttu-id="8b250-106">Для политики ssl все доступные параметры ssl-параметра **get-AzApplicationGatewayAvailableSlOption**</span><span class="sxs-lookup"><span data-stu-id="8b250-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="8b250-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8b250-107">EXAMPLES</span></span>

### <span data-ttu-id="8b250-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b250-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="8b250-109">Эти команды возвращают все доступные параметры ssl для политики ssl.</span><span class="sxs-lookup"><span data-stu-id="8b250-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="8b250-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b250-110">PARAMETERS</span></span>

### <span data-ttu-id="8b250-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b250-111">-DefaultProfile</span></span>
<span data-ttu-id="8b250-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b250-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b250-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b250-113">CommonParameters</span></span>
<span data-ttu-id="8b250-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b250-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b250-115">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b250-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b250-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b250-116">INPUTS</span></span>

### <span data-ttu-id="8b250-117">Нет</span><span class="sxs-lookup"><span data-stu-id="8b250-117">None</span></span>

## <span data-ttu-id="8b250-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b250-118">OUTPUTS</span></span>

### <span data-ttu-id="8b250-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="8b250-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="8b250-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8b250-120">NOTES</span></span>

## <span data-ttu-id="8b250-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b250-121">RELATED LINKS</span></span>
