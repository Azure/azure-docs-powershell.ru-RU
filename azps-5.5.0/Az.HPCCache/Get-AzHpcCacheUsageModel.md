---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccacheusagemodels
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
ms.openlocfilehash: 4552de7be0f2a489aa152a922e39df623736f842
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243485"
---
# <span data-ttu-id="c41ec-101">Get-AzHpcCacheUsageModel</span><span class="sxs-lookup"><span data-stu-id="c41ec-101">Get-AzHpcCacheUsageModel</span></span>

## <span data-ttu-id="c41ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c41ec-102">SYNOPSIS</span></span>
<span data-ttu-id="c41ec-103">Возвращает все показатели использования для целевого хранилища NFS.</span><span class="sxs-lookup"><span data-stu-id="c41ec-103">Gets all usageModels for NFS Storage Target.</span></span>

## <span data-ttu-id="c41ec-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c41ec-104">SYNTAX</span></span>

```
Get-AzHpcCacheUsageModel [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c41ec-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c41ec-105">DESCRIPTION</span></span>
<span data-ttu-id="c41ec-106">Cmdlet **Get-AzHpcCacheUsageModel** возвращает список моделей использования для целевого хранилища NFS.</span><span class="sxs-lookup"><span data-stu-id="c41ec-106">The **Get-AzHpcCacheUsageModel** cmdlet returns a list of usage models for NFS Storage Target.</span></span>

## <span data-ttu-id="c41ec-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c41ec-107">EXAMPLES</span></span>

### <span data-ttu-id="c41ec-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c41ec-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheUsageModel
```

## <span data-ttu-id="c41ec-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c41ec-109">PARAMETERS</span></span>

### <span data-ttu-id="c41ec-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c41ec-110">-DefaultProfile</span></span>
<span data-ttu-id="c41ec-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c41ec-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c41ec-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c41ec-112">CommonParameters</span></span>
<span data-ttu-id="c41ec-113">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c41ec-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c41ec-114">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c41ec-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c41ec-115">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c41ec-115">INPUTS</span></span>

### <span data-ttu-id="c41ec-116">Нет</span><span class="sxs-lookup"><span data-stu-id="c41ec-116">None</span></span>

## <span data-ttu-id="c41ec-117">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c41ec-117">OUTPUTS</span></span>

### <span data-ttu-id="c41ec-118">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcUsageModels</span><span class="sxs-lookup"><span data-stu-id="c41ec-118">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcUsageModels</span></span>

### <span data-ttu-id="c41ec-119">System.Object</span><span class="sxs-lookup"><span data-stu-id="c41ec-119">System.Object</span></span>
## <span data-ttu-id="c41ec-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c41ec-120">NOTES</span></span>

## <span data-ttu-id="c41ec-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c41ec-121">RELATED LINKS</span></span>
