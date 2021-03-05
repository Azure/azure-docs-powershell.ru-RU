---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/get-azhpccachesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheSku.md
ms.openlocfilehash: 65030abcc218e501a54de4ec27a3f557e32470de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012088"
---
# <span data-ttu-id="668cf-101">Get-AzHpcCacheSku</span><span class="sxs-lookup"><span data-stu-id="668cf-101">Get-AzHpcCacheSku</span></span>

## <span data-ttu-id="668cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="668cf-102">SYNOPSIS</span></span>
<span data-ttu-id="668cf-103">Все skus доступны в подписке.</span><span class="sxs-lookup"><span data-stu-id="668cf-103">Gets all SKUs available in subscription.</span></span>

## <span data-ttu-id="668cf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="668cf-104">SYNTAX</span></span>

```
Get-AzHpcCacheSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="668cf-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="668cf-105">DESCRIPTION</span></span>
<span data-ttu-id="668cf-106">Для **получения списка доступных** в подписке skus возвращается список доступных ВКП.</span><span class="sxs-lookup"><span data-stu-id="668cf-106">The **Get-AzHpcCacheSku** cmdlet returns a list of SKUs available in subscription.</span></span>

## <span data-ttu-id="668cf-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="668cf-107">EXAMPLES</span></span>

### <span data-ttu-id="668cf-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="668cf-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheSku
```

## <span data-ttu-id="668cf-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="668cf-109">PARAMETERS</span></span>

### <span data-ttu-id="668cf-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="668cf-110">-DefaultProfile</span></span>
<span data-ttu-id="668cf-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="668cf-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="668cf-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="668cf-112">CommonParameters</span></span>
<span data-ttu-id="668cf-113">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="668cf-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="668cf-114">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="668cf-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="668cf-115">INPUTS</span><span class="sxs-lookup"><span data-stu-id="668cf-115">INPUTS</span></span>

### <span data-ttu-id="668cf-116">Нет</span><span class="sxs-lookup"><span data-stu-id="668cf-116">None</span></span>

## <span data-ttu-id="668cf-117">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="668cf-117">OUTPUTS</span></span>

### <span data-ttu-id="668cf-118">Microsoft.Azure.Commands.HPCCache.PSSku</span><span class="sxs-lookup"><span data-stu-id="668cf-118">Microsoft.Azure.Commands.HPCCache.PSSku</span></span>

## <span data-ttu-id="668cf-119">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="668cf-119">NOTES</span></span>

## <span data-ttu-id="668cf-120">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="668cf-120">RELATED LINKS</span></span>
