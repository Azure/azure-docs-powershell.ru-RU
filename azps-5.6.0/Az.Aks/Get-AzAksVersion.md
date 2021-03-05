---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 3a46f28ad0f169f4f4f280922dff675b5e749fed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966899"
---
# <span data-ttu-id="1518d-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="1518d-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="1518d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1518d-102">SYNOPSIS</span></span>
<span data-ttu-id="1518d-103">Список доступных версий для создания кластера "Управляемые куберсети".</span><span class="sxs-lookup"><span data-stu-id="1518d-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="1518d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1518d-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1518d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1518d-105">DESCRIPTION</span></span>
<span data-ttu-id="1518d-106">Список доступных версий для создания кластера "Управляемые куберсети".</span><span class="sxs-lookup"><span data-stu-id="1518d-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="1518d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1518d-107">EXAMPLES</span></span>

### <span data-ttu-id="1518d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1518d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="1518d-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1518d-109">PARAMETERS</span></span>

### <span data-ttu-id="1518d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1518d-110">-DefaultProfile</span></span>
<span data-ttu-id="1518d-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1518d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1518d-112">-Location</span><span class="sxs-lookup"><span data-stu-id="1518d-112">-Location</span></span>
<span data-ttu-id="1518d-113">Расположение Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="1518d-113">Azure location for the cluster.</span></span>

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

### <span data-ttu-id="1518d-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1518d-114">CommonParameters</span></span>
<span data-ttu-id="1518d-115">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1518d-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1518d-116">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1518d-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1518d-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1518d-117">INPUTS</span></span>

### <span data-ttu-id="1518d-118">Нет</span><span class="sxs-lookup"><span data-stu-id="1518d-118">None</span></span>

## <span data-ttu-id="1518d-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1518d-119">OUTPUTS</span></span>

### <span data-ttu-id="1518d-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="1518d-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="1518d-121">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1518d-121">NOTES</span></span>

## <span data-ttu-id="1518d-122">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1518d-122">RELATED LINKS</span></span>
