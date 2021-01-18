---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheSku.md
ms.openlocfilehash: b9b9771cb5e06b4560dc436b738425288c0ad202
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506278"
---
# <span data-ttu-id="6c4b8-101">Get-AzHpcCacheSku</span><span class="sxs-lookup"><span data-stu-id="6c4b8-101">Get-AzHpcCacheSku</span></span>

## <span data-ttu-id="6c4b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c4b8-102">SYNOPSIS</span></span>
<span data-ttu-id="6c4b8-103">Все skus доступны в подписке.</span><span class="sxs-lookup"><span data-stu-id="6c4b8-103">Gets all SKUs available in subscription.</span></span>

## <span data-ttu-id="6c4b8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6c4b8-104">SYNTAX</span></span>

```
Get-AzHpcCacheSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c4b8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c4b8-105">DESCRIPTION</span></span>
<span data-ttu-id="6c4b8-106">Для **получения списка доступных** в подписке skus возвращается список доступных ВКП.</span><span class="sxs-lookup"><span data-stu-id="6c4b8-106">The **Get-AzHpcCacheSku** cmdlet returns a list of SKUs available in subscription.</span></span>

## <span data-ttu-id="6c4b8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6c4b8-107">EXAMPLES</span></span>

### <span data-ttu-id="6c4b8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6c4b8-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheSku
```

## <span data-ttu-id="6c4b8-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c4b8-109">PARAMETERS</span></span>

### <span data-ttu-id="6c4b8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c4b8-110">-DefaultProfile</span></span>
<span data-ttu-id="6c4b8-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c4b8-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c4b8-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c4b8-112">CommonParameters</span></span>
<span data-ttu-id="6c4b8-113">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c4b8-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c4b8-114">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c4b8-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c4b8-115">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c4b8-115">INPUTS</span></span>

### <span data-ttu-id="6c4b8-116">Нет</span><span class="sxs-lookup"><span data-stu-id="6c4b8-116">None</span></span>

## <span data-ttu-id="6c4b8-117">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6c4b8-117">OUTPUTS</span></span>

### <span data-ttu-id="6c4b8-118">Microsoft.Azure.Commands.HPCCache.PSSku</span><span class="sxs-lookup"><span data-stu-id="6c4b8-118">Microsoft.Azure.Commands.HPCCache.PSSku</span></span>

## <span data-ttu-id="6c4b8-119">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6c4b8-119">NOTES</span></span>

## <span data-ttu-id="6c4b8-120">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c4b8-120">RELATED LINKS</span></span>
