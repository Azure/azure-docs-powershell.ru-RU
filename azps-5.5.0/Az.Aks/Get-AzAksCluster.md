---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233953"
---
# <span data-ttu-id="39d1a-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="39d1a-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="39d1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39d1a-102">SYNOPSIS</span></span>
<span data-ttu-id="39d1a-103">Списки управляемых кластеров в кубберсетях.</span><span class="sxs-lookup"><span data-stu-id="39d1a-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="39d1a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="39d1a-104">SYNTAX</span></span>

### <span data-ttu-id="39d1a-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="39d1a-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="39d1a-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39d1a-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39d1a-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="39d1a-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39d1a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39d1a-108">DESCRIPTION</span></span>
<span data-ttu-id="39d1a-109">Списки управляемых кластеров в кубберсетях.</span><span class="sxs-lookup"><span data-stu-id="39d1a-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="39d1a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="39d1a-110">EXAMPLES</span></span>

### <span data-ttu-id="39d1a-111">Список всех кластеров куберсетей</span><span class="sxs-lookup"><span data-stu-id="39d1a-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="39d1a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39d1a-112">PARAMETERS</span></span>

### <span data-ttu-id="39d1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39d1a-113">-DefaultProfile</span></span>
<span data-ttu-id="39d1a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39d1a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39d1a-115">-Id</span><span class="sxs-lookup"><span data-stu-id="39d1a-115">-Id</span></span>
<span data-ttu-id="39d1a-116">ИД кластера "Управляемые кубберсети"</span><span class="sxs-lookup"><span data-stu-id="39d1a-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="39d1a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="39d1a-117">-Name</span></span>
<span data-ttu-id="39d1a-118">Название управляемого кластера "Кубберсети"</span><span class="sxs-lookup"><span data-stu-id="39d1a-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="39d1a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39d1a-119">-ResourceGroupName</span></span>
<span data-ttu-id="39d1a-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="39d1a-120">Resource group name</span></span>

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

### <span data-ttu-id="39d1a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d1a-121">CommonParameters</span></span>
<span data-ttu-id="39d1a-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39d1a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d1a-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39d1a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d1a-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39d1a-124">INPUTS</span></span>

### <span data-ttu-id="39d1a-125">System.String</span><span class="sxs-lookup"><span data-stu-id="39d1a-125">System.String</span></span>

## <span data-ttu-id="39d1a-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="39d1a-126">OUTPUTS</span></span>

### <span data-ttu-id="39d1a-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="39d1a-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="39d1a-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="39d1a-128">NOTES</span></span>

## <span data-ttu-id="39d1a-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39d1a-129">RELATED LINKS</span></span>
