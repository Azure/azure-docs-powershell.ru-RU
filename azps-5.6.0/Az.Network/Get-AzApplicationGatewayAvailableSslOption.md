---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: 8d2022f79dff5263f07737d525169dad3566fcda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003640"
---
# <span data-ttu-id="6f8d0-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="6f8d0-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="6f8d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f8d0-102">SYNOPSIS</span></span>
<span data-ttu-id="6f8d0-103">Все доступные параметры ssl для SSL-политики для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="6f8d0-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="6f8d0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6f8d0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f8d0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f8d0-105">DESCRIPTION</span></span>
<span data-ttu-id="6f8d0-106">Для политики ssl все доступные параметры ssl-параметра **get-AzApplicationGatewayAvailableSlOption**</span><span class="sxs-lookup"><span data-stu-id="6f8d0-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="6f8d0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6f8d0-107">EXAMPLES</span></span>

### <span data-ttu-id="6f8d0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6f8d0-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="6f8d0-109">Эти команды возвращают все доступные параметры ssl для политики ssl.</span><span class="sxs-lookup"><span data-stu-id="6f8d0-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="6f8d0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f8d0-110">PARAMETERS</span></span>

### <span data-ttu-id="6f8d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f8d0-111">-DefaultProfile</span></span>
<span data-ttu-id="6f8d0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f8d0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f8d0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f8d0-113">CommonParameters</span></span>
<span data-ttu-id="6f8d0-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f8d0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f8d0-115">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f8d0-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f8d0-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f8d0-116">INPUTS</span></span>

### <span data-ttu-id="6f8d0-117">Нет</span><span class="sxs-lookup"><span data-stu-id="6f8d0-117">None</span></span>

## <span data-ttu-id="6f8d0-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6f8d0-118">OUTPUTS</span></span>

### <span data-ttu-id="6f8d0-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSlOptions</span><span class="sxs-lookup"><span data-stu-id="6f8d0-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="6f8d0-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6f8d0-120">NOTES</span></span>

## <span data-ttu-id="6f8d0-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f8d0-121">RELATED LINKS</span></span>
