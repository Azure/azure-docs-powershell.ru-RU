---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 970cbb3e03a4934f648df2f6f8c06275a30740de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078154"
---
# <span data-ttu-id="06dc2-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="06dc2-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="06dc2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="06dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="06dc2-103">Список всех конфигураций вычислительных ресурсов</span><span class="sxs-lookup"><span data-stu-id="06dc2-103">List all compute resource Skus</span></span>

## <span data-ttu-id="06dc2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="06dc2-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06dc2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06dc2-105">DESCRIPTION</span></span>
<span data-ttu-id="06dc2-106">Список всех конфигураций вычислительных ресурсов</span><span class="sxs-lookup"><span data-stu-id="06dc2-106">List all compute resource Skus</span></span>

## <span data-ttu-id="06dc2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="06dc2-107">EXAMPLES</span></span>

### <span data-ttu-id="06dc2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="06dc2-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="06dc2-109">Список всех вычислительных конфигураций ресурсов в Западном регионе США</span><span class="sxs-lookup"><span data-stu-id="06dc2-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="06dc2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="06dc2-110">PARAMETERS</span></span>

### <span data-ttu-id="06dc2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06dc2-111">-DefaultProfile</span></span>
<span data-ttu-id="06dc2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06dc2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06dc2-113">-Location</span><span class="sxs-lookup"><span data-stu-id="06dc2-113">-Location</span></span>
<span data-ttu-id="06dc2-114">Указывает расположение доступных конфигураций для списка.</span><span class="sxs-lookup"><span data-stu-id="06dc2-114">Specifies a location of the available skus to list.</span></span>

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

### <span data-ttu-id="06dc2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06dc2-115">CommonParameters</span></span>
<span data-ttu-id="06dc2-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="06dc2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06dc2-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06dc2-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06dc2-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="06dc2-118">INPUTS</span></span>

### <span data-ttu-id="06dc2-119">System. String</span><span class="sxs-lookup"><span data-stu-id="06dc2-119">System.String</span></span>

## <span data-ttu-id="06dc2-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="06dc2-120">OUTPUTS</span></span>

### <span data-ttu-id="06dc2-121">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="06dc2-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="06dc2-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="06dc2-122">NOTES</span></span>

## <span data-ttu-id="06dc2-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06dc2-123">RELATED LINKS</span></span>
