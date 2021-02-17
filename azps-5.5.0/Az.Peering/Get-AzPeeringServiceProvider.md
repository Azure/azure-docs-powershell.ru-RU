---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: 8341f465bab88f8d8a60e5f171f883dbb9a2467e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236348"
---
# <span data-ttu-id="d14d4-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="d14d4-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="d14d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d14d4-102">SYNOPSIS</span></span>
<span data-ttu-id="d14d4-103">Получает список поставщиков услуг пиринга, партнерских с Корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="d14d4-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="d14d4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d14d4-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d14d4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d14d4-105">DESCRIPTION</span></span>
<span data-ttu-id="d14d4-106">Поставщики пиринга списков</span><span class="sxs-lookup"><span data-stu-id="d14d4-106">List peering service providers</span></span>

## <span data-ttu-id="d14d4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d14d4-107">EXAMPLES</span></span>

### <span data-ttu-id="d14d4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d14d4-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="d14d4-109">Доступно поставщиков услуг пиринга</span><span class="sxs-lookup"><span data-stu-id="d14d4-109">Gets available peering service providers</span></span>

## <span data-ttu-id="d14d4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d14d4-110">PARAMETERS</span></span>

### <span data-ttu-id="d14d4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d14d4-111">-DefaultProfile</span></span>
<span data-ttu-id="d14d4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d14d4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d14d4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d14d4-113">CommonParameters</span></span>
<span data-ttu-id="d14d4-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d14d4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d14d4-115">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d14d4-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d14d4-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d14d4-116">INPUTS</span></span>

### <span data-ttu-id="d14d4-117">Нет</span><span class="sxs-lookup"><span data-stu-id="d14d4-117">None</span></span>

## <span data-ttu-id="d14d4-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d14d4-118">OUTPUTS</span></span>

### <span data-ttu-id="d14d4-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="d14d4-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="d14d4-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d14d4-120">NOTES</span></span>

## <span data-ttu-id="d14d4-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d14d4-121">RELATED LINKS</span></span>
