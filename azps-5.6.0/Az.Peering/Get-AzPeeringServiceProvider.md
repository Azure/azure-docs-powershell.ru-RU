---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: cfc25f735d2785a688f29fd3eb3064337b5c6e8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989467"
---
# <span data-ttu-id="f8354-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="f8354-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="f8354-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8354-102">SYNOPSIS</span></span>
<span data-ttu-id="f8354-103">Получает список поставщиков услуг пиринга, партнерских с Корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="f8354-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="f8354-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f8354-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8354-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8354-105">DESCRIPTION</span></span>
<span data-ttu-id="f8354-106">Поставщики пиринга списков</span><span class="sxs-lookup"><span data-stu-id="f8354-106">List peering service providers</span></span>

## <span data-ttu-id="f8354-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f8354-107">EXAMPLES</span></span>

### <span data-ttu-id="f8354-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f8354-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="f8354-109">Доступно поставщиков услуг пиринга</span><span class="sxs-lookup"><span data-stu-id="f8354-109">Gets available peering service providers</span></span>

## <span data-ttu-id="f8354-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8354-110">PARAMETERS</span></span>

### <span data-ttu-id="f8354-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8354-111">-DefaultProfile</span></span>
<span data-ttu-id="f8354-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8354-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8354-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8354-113">CommonParameters</span></span>
<span data-ttu-id="f8354-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8354-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8354-115">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8354-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8354-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8354-116">INPUTS</span></span>

### <span data-ttu-id="f8354-117">Нет</span><span class="sxs-lookup"><span data-stu-id="f8354-117">None</span></span>

## <span data-ttu-id="f8354-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f8354-118">OUTPUTS</span></span>

### <span data-ttu-id="f8354-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="f8354-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="f8354-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f8354-120">NOTES</span></span>

## <span data-ttu-id="f8354-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8354-121">RELATED LINKS</span></span>
