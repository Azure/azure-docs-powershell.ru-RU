---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 970cbb3e03a4934f648df2f6f8c06275a30740de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229124"
---
# <span data-ttu-id="cd749-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="cd749-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="cd749-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd749-102">SYNOPSIS</span></span>
<span data-ttu-id="cd749-103">List all compute resource Skus</span><span class="sxs-lookup"><span data-stu-id="cd749-103">List all compute resource Skus</span></span>

## <span data-ttu-id="cd749-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cd749-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd749-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd749-105">DESCRIPTION</span></span>
<span data-ttu-id="cd749-106">List all compute resource Skus</span><span class="sxs-lookup"><span data-stu-id="cd749-106">List all compute resource Skus</span></span>

## <span data-ttu-id="cd749-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cd749-107">EXAMPLES</span></span>

### <span data-ttu-id="cd749-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cd749-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="cd749-109">List all compute resource skus in West US region</span><span class="sxs-lookup"><span data-stu-id="cd749-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="cd749-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd749-110">PARAMETERS</span></span>

### <span data-ttu-id="cd749-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd749-111">-DefaultProfile</span></span>
<span data-ttu-id="cd749-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd749-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd749-113">-Location</span><span class="sxs-lookup"><span data-stu-id="cd749-113">-Location</span></span>
<span data-ttu-id="cd749-114">Определяет расположение доступных skus для списка.</span><span class="sxs-lookup"><span data-stu-id="cd749-114">Specifies a location of the available skus to list.</span></span>

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

### <span data-ttu-id="cd749-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd749-115">CommonParameters</span></span>
<span data-ttu-id="cd749-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd749-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd749-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd749-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd749-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd749-118">INPUTS</span></span>

### <span data-ttu-id="cd749-119">System.String</span><span class="sxs-lookup"><span data-stu-id="cd749-119">System.String</span></span>

## <span data-ttu-id="cd749-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cd749-120">OUTPUTS</span></span>

### <span data-ttu-id="cd749-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="cd749-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="cd749-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cd749-122">NOTES</span></span>

## <span data-ttu-id="cd749-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd749-123">RELATED LINKS</span></span>
