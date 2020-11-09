---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 704e95cdd01291fb617a6f0c22a051daa69434d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247115"
---
# <span data-ttu-id="e51ae-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="e51ae-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="e51ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e51ae-102">SYNOPSIS</span></span>
<span data-ttu-id="e51ae-103">Список доступных версий для создания управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e51ae-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e51ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e51ae-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e51ae-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e51ae-105">DESCRIPTION</span></span>
<span data-ttu-id="e51ae-106">Список доступных версий для создания управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e51ae-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e51ae-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e51ae-107">EXAMPLES</span></span>

### <span data-ttu-id="e51ae-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e51ae-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="e51ae-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e51ae-109">PARAMETERS</span></span>

### <span data-ttu-id="e51ae-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e51ae-110">-DefaultProfile</span></span>
<span data-ttu-id="e51ae-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e51ae-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e51ae-112">-Location</span><span class="sxs-lookup"><span data-stu-id="e51ae-112">-Location</span></span>
<span data-ttu-id="e51ae-113">Расположение Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="e51ae-113">Azure location for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51ae-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e51ae-114">CommonParameters</span></span>
<span data-ttu-id="e51ae-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e51ae-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e51ae-116">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e51ae-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e51ae-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e51ae-117">INPUTS</span></span>

### <span data-ttu-id="e51ae-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="e51ae-118">None</span></span>

## <span data-ttu-id="e51ae-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e51ae-119">OUTPUTS</span></span>

### <span data-ttu-id="e51ae-120">Microsoft. Azure. Commands. AKS. Models. PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="e51ae-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="e51ae-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="e51ae-121">NOTES</span></span>

## <span data-ttu-id="e51ae-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e51ae-122">RELATED LINKS</span></span>