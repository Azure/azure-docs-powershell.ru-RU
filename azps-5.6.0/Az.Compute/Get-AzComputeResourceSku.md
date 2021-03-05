---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: e2b3dd89152b376ac12826eeb342c80486c2c39a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983752"
---
# <span data-ttu-id="204f1-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="204f1-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="204f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="204f1-102">SYNOPSIS</span></span>
<span data-ttu-id="204f1-103">List all compute resource Skus</span><span class="sxs-lookup"><span data-stu-id="204f1-103">List all compute resource Skus</span></span>

## <span data-ttu-id="204f1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="204f1-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="204f1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="204f1-105">DESCRIPTION</span></span>
<span data-ttu-id="204f1-106">List all compute resource Skus</span><span class="sxs-lookup"><span data-stu-id="204f1-106">List all compute resource Skus</span></span>

## <span data-ttu-id="204f1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="204f1-107">EXAMPLES</span></span>

### <span data-ttu-id="204f1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="204f1-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="204f1-109">Список всех усов вычислительных ресурсов в регионе "Запад США"</span><span class="sxs-lookup"><span data-stu-id="204f1-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="204f1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="204f1-110">PARAMETERS</span></span>

### <span data-ttu-id="204f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="204f1-111">-DefaultProfile</span></span>
<span data-ttu-id="204f1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="204f1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="204f1-113">-Location</span><span class="sxs-lookup"><span data-stu-id="204f1-113">-Location</span></span>
<span data-ttu-id="204f1-114">Определяет расположение доступных skus для списка.</span><span class="sxs-lookup"><span data-stu-id="204f1-114">Specifies a location of the available skus to list.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="204f1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="204f1-115">CommonParameters</span></span>
<span data-ttu-id="204f1-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="204f1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="204f1-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="204f1-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="204f1-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="204f1-118">INPUTS</span></span>

### <span data-ttu-id="204f1-119">System.String</span><span class="sxs-lookup"><span data-stu-id="204f1-119">System.String</span></span>

## <span data-ttu-id="204f1-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="204f1-120">OUTPUTS</span></span>

### <span data-ttu-id="204f1-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="204f1-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="204f1-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="204f1-122">NOTES</span></span>

## <span data-ttu-id="204f1-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="204f1-123">RELATED LINKS</span></span>
