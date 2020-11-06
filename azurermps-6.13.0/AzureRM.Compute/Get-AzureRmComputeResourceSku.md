---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: cf10674f3140e618b82b40e6c8288126cb941c3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561095"
---
# <span data-ttu-id="328c6-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="328c6-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="328c6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="328c6-102">SYNOPSIS</span></span>
<span data-ttu-id="328c6-103">Список всех конфигураций вычислительных ресурсов</span><span class="sxs-lookup"><span data-stu-id="328c6-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="328c6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="328c6-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="328c6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="328c6-105">DESCRIPTION</span></span>
<span data-ttu-id="328c6-106">Список всех конфигураций вычислительных ресурсов</span><span class="sxs-lookup"><span data-stu-id="328c6-106">List all compute resource Skus</span></span>

## <span data-ttu-id="328c6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="328c6-107">EXAMPLES</span></span>

### <span data-ttu-id="328c6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="328c6-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="328c6-109">Список всех вычислительных конфигураций ресурсов в Западном регионе США</span><span class="sxs-lookup"><span data-stu-id="328c6-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="328c6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="328c6-110">PARAMETERS</span></span>

### <span data-ttu-id="328c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="328c6-111">-DefaultProfile</span></span>
<span data-ttu-id="328c6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="328c6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="328c6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="328c6-113">CommonParameters</span></span>
<span data-ttu-id="328c6-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="328c6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="328c6-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="328c6-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="328c6-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="328c6-116">INPUTS</span></span>

### <span data-ttu-id="328c6-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="328c6-117">None</span></span>

## <span data-ttu-id="328c6-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="328c6-118">OUTPUTS</span></span>

### <span data-ttu-id="328c6-119">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="328c6-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="328c6-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="328c6-120">NOTES</span></span>

## <span data-ttu-id="328c6-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="328c6-121">RELATED LINKS</span></span>
