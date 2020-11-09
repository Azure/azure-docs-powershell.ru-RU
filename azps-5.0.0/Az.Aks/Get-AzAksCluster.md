---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247895"
---
# <span data-ttu-id="60ec1-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="60ec1-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="60ec1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="60ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="60ec1-103">Перечислите Kubernetes управляемые кластеры.</span><span class="sxs-lookup"><span data-stu-id="60ec1-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="60ec1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="60ec1-104">SYNTAX</span></span>

### <span data-ttu-id="60ec1-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="60ec1-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60ec1-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60ec1-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60ec1-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="60ec1-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60ec1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60ec1-108">DESCRIPTION</span></span>
<span data-ttu-id="60ec1-109">Перечислите Kubernetes управляемые кластеры.</span><span class="sxs-lookup"><span data-stu-id="60ec1-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="60ec1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="60ec1-110">EXAMPLES</span></span>

### <span data-ttu-id="60ec1-111">Список всех кластеров Kubernetes</span><span class="sxs-lookup"><span data-stu-id="60ec1-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="60ec1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="60ec1-112">PARAMETERS</span></span>

### <span data-ttu-id="60ec1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60ec1-113">-DefaultProfile</span></span>
<span data-ttu-id="60ec1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60ec1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60ec1-115">-ID</span><span class="sxs-lookup"><span data-stu-id="60ec1-115">-Id</span></span>
<span data-ttu-id="60ec1-116">Идентификатор управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="60ec1-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="60ec1-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="60ec1-117">-Name</span></span>
<span data-ttu-id="60ec1-118">Имя управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="60ec1-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="60ec1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60ec1-119">-ResourceGroupName</span></span>
<span data-ttu-id="60ec1-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="60ec1-120">Resource group name</span></span>

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

### <span data-ttu-id="60ec1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60ec1-121">CommonParameters</span></span>
<span data-ttu-id="60ec1-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="60ec1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60ec1-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60ec1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60ec1-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="60ec1-124">INPUTS</span></span>

### <span data-ttu-id="60ec1-125">System. String</span><span class="sxs-lookup"><span data-stu-id="60ec1-125">System.String</span></span>

## <span data-ttu-id="60ec1-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="60ec1-126">OUTPUTS</span></span>

### <span data-ttu-id="60ec1-127">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="60ec1-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="60ec1-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="60ec1-128">NOTES</span></span>

## <span data-ttu-id="60ec1-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60ec1-129">RELATED LINKS</span></span>