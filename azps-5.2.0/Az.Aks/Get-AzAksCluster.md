---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399444"
---
# <span data-ttu-id="c7db5-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="c7db5-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="c7db5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7db5-102">SYNOPSIS</span></span>
<span data-ttu-id="c7db5-103">Списки управляемых кластеров в кубберсетях.</span><span class="sxs-lookup"><span data-stu-id="c7db5-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="c7db5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c7db5-104">SYNTAX</span></span>

### <span data-ttu-id="c7db5-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c7db5-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7db5-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7db5-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7db5-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7db5-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7db5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7db5-108">DESCRIPTION</span></span>
<span data-ttu-id="c7db5-109">Списки управляемых кластеров в кубберсетях.</span><span class="sxs-lookup"><span data-stu-id="c7db5-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="c7db5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c7db5-110">EXAMPLES</span></span>

### <span data-ttu-id="c7db5-111">Список всех кластеров куберсетей</span><span class="sxs-lookup"><span data-stu-id="c7db5-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="c7db5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7db5-112">PARAMETERS</span></span>

### <span data-ttu-id="c7db5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7db5-113">-DefaultProfile</span></span>
<span data-ttu-id="c7db5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7db5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7db5-115">-Id</span><span class="sxs-lookup"><span data-stu-id="c7db5-115">-Id</span></span>
<span data-ttu-id="c7db5-116">ИД кластера "Управляемые кубберсети"</span><span class="sxs-lookup"><span data-stu-id="c7db5-116">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7db5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c7db5-117">-Name</span></span>
<span data-ttu-id="c7db5-118">Название управляемого кластера "Кубберсети"</span><span class="sxs-lookup"><span data-stu-id="c7db5-118">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7db5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7db5-119">-ResourceGroupName</span></span>
<span data-ttu-id="c7db5-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c7db5-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7db5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7db5-121">CommonParameters</span></span>
<span data-ttu-id="c7db5-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7db5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7db5-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7db5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7db5-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7db5-124">INPUTS</span></span>

### <span data-ttu-id="c7db5-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c7db5-125">System.String</span></span>

## <span data-ttu-id="c7db5-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c7db5-126">OUTPUTS</span></span>

### <span data-ttu-id="c7db5-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="c7db5-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="c7db5-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c7db5-128">NOTES</span></span>

## <span data-ttu-id="c7db5-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7db5-129">RELATED LINKS</span></span>
