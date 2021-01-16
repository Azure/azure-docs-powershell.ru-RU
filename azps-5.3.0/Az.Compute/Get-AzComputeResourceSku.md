---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 970cbb3e03a4934f648df2f6f8c06275a30740de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509221"
---
# <span data-ttu-id="35ed8-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="35ed8-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="35ed8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="35ed8-103">List all compute resource Skus</span><span class="sxs-lookup"><span data-stu-id="35ed8-103">List all compute resource Skus</span></span>

## <span data-ttu-id="35ed8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35ed8-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35ed8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35ed8-105">DESCRIPTION</span></span>
<span data-ttu-id="35ed8-106">List all compute resource Skus</span><span class="sxs-lookup"><span data-stu-id="35ed8-106">List all compute resource Skus</span></span>

## <span data-ttu-id="35ed8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35ed8-107">EXAMPLES</span></span>

### <span data-ttu-id="35ed8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="35ed8-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="35ed8-109">Список всех усов вычислительных ресурсов в регионе "Запад США"</span><span class="sxs-lookup"><span data-stu-id="35ed8-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="35ed8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35ed8-110">PARAMETERS</span></span>

### <span data-ttu-id="35ed8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ed8-111">-DefaultProfile</span></span>
<span data-ttu-id="35ed8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35ed8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35ed8-113">-Location</span><span class="sxs-lookup"><span data-stu-id="35ed8-113">-Location</span></span>
<span data-ttu-id="35ed8-114">Определяет расположение доступных skus для списка.</span><span class="sxs-lookup"><span data-stu-id="35ed8-114">Specifies a location of the available skus to list.</span></span>

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

### <span data-ttu-id="35ed8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ed8-115">CommonParameters</span></span>
<span data-ttu-id="35ed8-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35ed8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ed8-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35ed8-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ed8-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35ed8-118">INPUTS</span></span>

### <span data-ttu-id="35ed8-119">System.String</span><span class="sxs-lookup"><span data-stu-id="35ed8-119">System.String</span></span>

## <span data-ttu-id="35ed8-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35ed8-120">OUTPUTS</span></span>

### <span data-ttu-id="35ed8-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="35ed8-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="35ed8-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35ed8-122">NOTES</span></span>

## <span data-ttu-id="35ed8-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35ed8-123">RELATED LINKS</span></span>
