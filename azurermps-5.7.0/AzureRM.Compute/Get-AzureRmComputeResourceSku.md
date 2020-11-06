---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: b9e1c42ca3a67a80a939a4e79626253b903764f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559223"
---
# <span data-ttu-id="8ac2b-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="8ac2b-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="8ac2b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ac2b-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac2b-103">Список всех конфигураций вычислительных ресурсов</span><span class="sxs-lookup"><span data-stu-id="8ac2b-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ac2b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ac2b-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [<CommonParameters>]
```

## <span data-ttu-id="8ac2b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ac2b-105">DESCRIPTION</span></span>
<span data-ttu-id="8ac2b-106">Список всех конфигураций вычислительных ресурсов</span><span class="sxs-lookup"><span data-stu-id="8ac2b-106">List all compute resource Skus</span></span>

## <span data-ttu-id="8ac2b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ac2b-107">EXAMPLES</span></span>

### <span data-ttu-id="8ac2b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8ac2b-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="8ac2b-109">Список всех вычислительных конфигураций ресурсов в Западном регионе США</span><span class="sxs-lookup"><span data-stu-id="8ac2b-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="8ac2b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ac2b-110">PARAMETERS</span></span>

### <span data-ttu-id="8ac2b-111">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac2b-111">CommonParameters</span></span>
<span data-ttu-id="8ac2b-112">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ac2b-112">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac2b-113">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ac2b-113">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac2b-114">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ac2b-114">INPUTS</span></span>

### <span data-ttu-id="8ac2b-115">Ничего</span><span class="sxs-lookup"><span data-stu-id="8ac2b-115">None</span></span>


## <span data-ttu-id="8ac2b-116">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ac2b-116">OUTPUTS</span></span>

### <span data-ttu-id="8ac2b-117">System. Object</span><span class="sxs-lookup"><span data-stu-id="8ac2b-117">System.Object</span></span>

## <span data-ttu-id="8ac2b-118">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ac2b-118">NOTES</span></span>

## <span data-ttu-id="8ac2b-119">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ac2b-119">RELATED LINKS</span></span>

