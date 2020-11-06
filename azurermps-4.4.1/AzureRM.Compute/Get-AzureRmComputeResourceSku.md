---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: fd4a06375a4dfab7f8b8cd4b08a2112310e99b73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568815"
---
# <span data-ttu-id="158f1-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="158f1-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="158f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="158f1-102">SYNOPSIS</span></span>
<span data-ttu-id="158f1-103">Список всех конфигураций вычислительных ресурсов</span><span class="sxs-lookup"><span data-stu-id="158f1-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="158f1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="158f1-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="158f1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="158f1-105">DESCRIPTION</span></span>
<span data-ttu-id="158f1-106">Список всех конфигураций вычислительных ресурсов</span><span class="sxs-lookup"><span data-stu-id="158f1-106">List all compute resource Skus</span></span>

## <span data-ttu-id="158f1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="158f1-107">EXAMPLES</span></span>

### <span data-ttu-id="158f1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="158f1-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="158f1-109">Список всех вычислительных конфигураций ресурсов в Западном регионе США</span><span class="sxs-lookup"><span data-stu-id="158f1-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="158f1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="158f1-110">PARAMETERS</span></span>

### <span data-ttu-id="158f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="158f1-111">-DefaultProfile</span></span>
<span data-ttu-id="158f1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="158f1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="158f1-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="158f1-113">CommonParameters</span></span>
<span data-ttu-id="158f1-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="158f1-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="158f1-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="158f1-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="158f1-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="158f1-116">INPUTS</span></span>

### <span data-ttu-id="158f1-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="158f1-117">None</span></span>

## <span data-ttu-id="158f1-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="158f1-118">OUTPUTS</span></span>

### <span data-ttu-id="158f1-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="158f1-119">System.Object</span></span>

## <span data-ttu-id="158f1-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="158f1-120">NOTES</span></span>

## <span data-ttu-id="158f1-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="158f1-121">RELATED LINKS</span></span>

