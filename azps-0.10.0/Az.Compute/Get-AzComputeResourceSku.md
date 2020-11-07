---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 751a551f5ed0a0a1968c74e5f94bcabad3b5ff32
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911561"
---
# <span data-ttu-id="67b26-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="67b26-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="67b26-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67b26-102">SYNOPSIS</span></span>
<span data-ttu-id="67b26-103">Список всех конфигураций вычислительных ресурсов</span><span class="sxs-lookup"><span data-stu-id="67b26-103">List all compute resource Skus</span></span>

## <span data-ttu-id="67b26-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67b26-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67b26-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67b26-105">DESCRIPTION</span></span>
<span data-ttu-id="67b26-106">Список всех конфигураций вычислительных ресурсов</span><span class="sxs-lookup"><span data-stu-id="67b26-106">List all compute resource Skus</span></span>

## <span data-ttu-id="67b26-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67b26-107">EXAMPLES</span></span>

### <span data-ttu-id="67b26-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="67b26-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="67b26-109">Список всех вычислительных конфигураций ресурсов в Западном регионе США</span><span class="sxs-lookup"><span data-stu-id="67b26-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="67b26-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67b26-110">PARAMETERS</span></span>

### <span data-ttu-id="67b26-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67b26-111">-DefaultProfile</span></span>
<span data-ttu-id="67b26-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67b26-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b26-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67b26-113">CommonParameters</span></span>
<span data-ttu-id="67b26-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67b26-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67b26-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67b26-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67b26-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67b26-116">INPUTS</span></span>

### <span data-ttu-id="67b26-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="67b26-117">None</span></span>

## <span data-ttu-id="67b26-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67b26-118">OUTPUTS</span></span>

### <span data-ttu-id="67b26-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="67b26-119">System.Object</span></span>

## <span data-ttu-id="67b26-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="67b26-120">NOTES</span></span>

## <span data-ttu-id="67b26-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67b26-121">RELATED LINKS</span></span>

