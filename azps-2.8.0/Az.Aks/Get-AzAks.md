---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
ms.openlocfilehash: 34db847ba7a4051efab32a62c667d3d79ad4ac30
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728210"
---
# <span data-ttu-id="c97ef-101">Get-AzAks</span><span class="sxs-lookup"><span data-stu-id="c97ef-101">Get-AzAks</span></span>

## <span data-ttu-id="c97ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c97ef-102">SYNOPSIS</span></span>
<span data-ttu-id="c97ef-103">Перечислите Kubernetes управляемые кластеры.</span><span class="sxs-lookup"><span data-stu-id="c97ef-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="c97ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c97ef-104">SYNTAX</span></span>

### <span data-ttu-id="c97ef-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c97ef-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c97ef-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c97ef-106">IdParameterSet</span></span>
```
Get-AzAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c97ef-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c97ef-107">NameParameterSet</span></span>
```
Get-AzAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c97ef-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c97ef-108">DESCRIPTION</span></span>
<span data-ttu-id="c97ef-109">Перечислите Kubernetes управляемые кластеры.</span><span class="sxs-lookup"><span data-stu-id="c97ef-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="c97ef-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c97ef-110">EXAMPLES</span></span>

### <span data-ttu-id="c97ef-111">Список всех кластеров Kubernetes</span><span class="sxs-lookup"><span data-stu-id="c97ef-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzAks
```

## <span data-ttu-id="c97ef-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c97ef-112">PARAMETERS</span></span>

### <span data-ttu-id="c97ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c97ef-113">-DefaultProfile</span></span>
<span data-ttu-id="c97ef-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c97ef-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c97ef-115">-ID</span><span class="sxs-lookup"><span data-stu-id="c97ef-115">-Id</span></span>
<span data-ttu-id="c97ef-116">Идентификатор управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="c97ef-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="c97ef-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c97ef-117">-Name</span></span>
<span data-ttu-id="c97ef-118">Имя управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="c97ef-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="c97ef-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c97ef-119">-ResourceGroupName</span></span>
<span data-ttu-id="c97ef-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c97ef-120">Resource group name</span></span>

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

### <span data-ttu-id="c97ef-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c97ef-121">CommonParameters</span></span>
<span data-ttu-id="c97ef-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c97ef-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c97ef-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c97ef-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c97ef-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c97ef-124">INPUTS</span></span>

### <span data-ttu-id="c97ef-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c97ef-125">System.String</span></span>

## <span data-ttu-id="c97ef-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c97ef-126">OUTPUTS</span></span>

### <span data-ttu-id="c97ef-127">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="c97ef-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="c97ef-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="c97ef-128">NOTES</span></span>

## <span data-ttu-id="c97ef-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c97ef-129">RELATED LINKS</span></span>
