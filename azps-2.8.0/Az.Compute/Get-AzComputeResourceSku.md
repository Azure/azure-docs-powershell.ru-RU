---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: e3c33fb3d61479531303389defb0d7ebdbb3fb64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727482"
---
# <span data-ttu-id="37f9e-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="37f9e-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="37f9e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37f9e-102">SYNOPSIS</span></span>
<span data-ttu-id="37f9e-103">Список всех конфигураций вычислительных ресурсов</span><span class="sxs-lookup"><span data-stu-id="37f9e-103">List all compute resource Skus</span></span>

## <span data-ttu-id="37f9e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37f9e-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37f9e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37f9e-105">DESCRIPTION</span></span>
<span data-ttu-id="37f9e-106">Список всех конфигураций вычислительных ресурсов</span><span class="sxs-lookup"><span data-stu-id="37f9e-106">List all compute resource Skus</span></span>

## <span data-ttu-id="37f9e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37f9e-107">EXAMPLES</span></span>

### <span data-ttu-id="37f9e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="37f9e-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="37f9e-109">Список всех вычислительных конфигураций ресурсов в Западном регионе США</span><span class="sxs-lookup"><span data-stu-id="37f9e-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="37f9e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37f9e-110">PARAMETERS</span></span>

### <span data-ttu-id="37f9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37f9e-111">-DefaultProfile</span></span>
<span data-ttu-id="37f9e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37f9e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37f9e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37f9e-113">CommonParameters</span></span>
<span data-ttu-id="37f9e-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37f9e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37f9e-115">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37f9e-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37f9e-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37f9e-116">INPUTS</span></span>

### <span data-ttu-id="37f9e-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="37f9e-117">None</span></span>

## <span data-ttu-id="37f9e-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37f9e-118">OUTPUTS</span></span>

### <span data-ttu-id="37f9e-119">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="37f9e-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="37f9e-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="37f9e-120">NOTES</span></span>

## <span data-ttu-id="37f9e-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37f9e-121">RELATED LINKS</span></span>
