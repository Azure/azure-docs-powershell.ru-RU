---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcomputeresourcesku
schema: 2.0.0
ms.openlocfilehash: e7ebc6a8e6b59679757f559ff2d09ebaa8c5475f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915406"
---
# <span data-ttu-id="42746-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="42746-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="42746-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42746-102">SYNOPSIS</span></span>
<span data-ttu-id="42746-103">Список всех конфигураций вычислительных ресурсов</span><span class="sxs-lookup"><span data-stu-id="42746-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42746-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42746-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42746-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42746-105">DESCRIPTION</span></span>
<span data-ttu-id="42746-106">Список всех конфигураций вычислительных ресурсов</span><span class="sxs-lookup"><span data-stu-id="42746-106">List all compute resource Skus</span></span>

## <span data-ttu-id="42746-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42746-107">EXAMPLES</span></span>

### <span data-ttu-id="42746-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="42746-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="42746-109">Список всех вычислительных конфигураций ресурсов в Западном регионе США</span><span class="sxs-lookup"><span data-stu-id="42746-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="42746-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42746-110">PARAMETERS</span></span>

### <span data-ttu-id="42746-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42746-111">-DefaultProfile</span></span>
<span data-ttu-id="42746-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42746-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42746-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42746-113">CommonParameters</span></span>
<span data-ttu-id="42746-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42746-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42746-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42746-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42746-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42746-116">INPUTS</span></span>

### <span data-ttu-id="42746-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="42746-117">None</span></span>

## <span data-ttu-id="42746-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42746-118">OUTPUTS</span></span>

### <span data-ttu-id="42746-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="42746-119">System.Object</span></span>

## <span data-ttu-id="42746-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="42746-120">NOTES</span></span>

## <span data-ttu-id="42746-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42746-121">RELATED LINKS</span></span>

