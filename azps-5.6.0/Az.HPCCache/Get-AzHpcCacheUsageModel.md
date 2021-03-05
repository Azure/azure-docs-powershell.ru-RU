---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/get-azhpccacheusagemodels
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
ms.openlocfilehash: 51b7297aea0378b910d647f892a252a9b2ce494b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013544"
---
# <span data-ttu-id="55279-101">Get-AzHpcCacheUsageModel</span><span class="sxs-lookup"><span data-stu-id="55279-101">Get-AzHpcCacheUsageModel</span></span>

## <span data-ttu-id="55279-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55279-102">SYNOPSIS</span></span>
<span data-ttu-id="55279-103">Возвращает все показатели использования для целевого хранилища NFS.</span><span class="sxs-lookup"><span data-stu-id="55279-103">Gets all usageModels for NFS Storage Target.</span></span>

## <span data-ttu-id="55279-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="55279-104">SYNTAX</span></span>

```
Get-AzHpcCacheUsageModel [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55279-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55279-105">DESCRIPTION</span></span>
<span data-ttu-id="55279-106">Cmdlet **Get-AzHpcCacheUsageModel** возвращает список моделей использования для целевого хранилища NFS.</span><span class="sxs-lookup"><span data-stu-id="55279-106">The **Get-AzHpcCacheUsageModel** cmdlet returns a list of usage models for NFS Storage Target.</span></span>

## <span data-ttu-id="55279-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="55279-107">EXAMPLES</span></span>

### <span data-ttu-id="55279-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="55279-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheUsageModel
```

## <span data-ttu-id="55279-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55279-109">PARAMETERS</span></span>

### <span data-ttu-id="55279-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55279-110">-DefaultProfile</span></span>
<span data-ttu-id="55279-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55279-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55279-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55279-112">CommonParameters</span></span>
<span data-ttu-id="55279-113">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55279-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55279-114">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55279-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55279-115">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55279-115">INPUTS</span></span>

### <span data-ttu-id="55279-116">Нет</span><span class="sxs-lookup"><span data-stu-id="55279-116">None</span></span>

## <span data-ttu-id="55279-117">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="55279-117">OUTPUTS</span></span>

### <span data-ttu-id="55279-118">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcUsageModels</span><span class="sxs-lookup"><span data-stu-id="55279-118">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcUsageModels</span></span>

### <span data-ttu-id="55279-119">System.Object</span><span class="sxs-lookup"><span data-stu-id="55279-119">System.Object</span></span>
## <span data-ttu-id="55279-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="55279-120">NOTES</span></span>

## <span data-ttu-id="55279-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55279-121">RELATED LINKS</span></span>
