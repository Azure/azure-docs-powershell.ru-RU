---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.ADDomainServices/new-AzADDomainServiceReplicaSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
ms.openlocfilehash: ad11cbe364cd4d9cd8a667fd40a6a1d438f1aed4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986306"
---
# <span data-ttu-id="76b13-101">New-AzADDomainServiceReplicaSet</span><span class="sxs-lookup"><span data-stu-id="76b13-101">New-AzADDomainServiceReplicaSet</span></span>

## <span data-ttu-id="76b13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76b13-102">SYNOPSIS</span></span>
<span data-ttu-id="76b13-103">Создание в памяти объекта для ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="76b13-103">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="76b13-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="76b13-104">SYNTAX</span></span>

```
New-AzADDomainServiceReplicaSet [-Location <String>] [-SubnetId <String>] [<CommonParameters>]
```

## <span data-ttu-id="76b13-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76b13-105">DESCRIPTION</span></span>
<span data-ttu-id="76b13-106">Создание в памяти объекта для ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="76b13-106">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="76b13-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="76b13-107">EXAMPLES</span></span>

### <span data-ttu-id="76b13-108">Пример 1. Создание репликации для AdDomain</span><span class="sxs-lookup"><span data-stu-id="76b13-108">Example 1: Create ReplicaSet for AdDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceReplicaSet -Location eastus -SubnetId /subscriptions/**********-****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/Microsoft.Network/virtualNetworks/yourinttest/subnets/default

DomainControllerIPAddress ExternalAccessIPAddress HealthLastEvaluated Location ServiceStatus SubnetId
------------------------- ----------------------- ------------------- -------- ------------- --------
                                                                      eastus                 /subscriptions/****
                                                                      ****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/M…
```

<span data-ttu-id="76b13-109">Создать ReplicaSet для AdDomain</span><span class="sxs-lookup"><span data-stu-id="76b13-109">Create ReplicaSet for AdDomain</span></span>

## <span data-ttu-id="76b13-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76b13-110">PARAMETERS</span></span>

### <span data-ttu-id="76b13-111">-Location</span><span class="sxs-lookup"><span data-stu-id="76b13-111">-Location</span></span>
<span data-ttu-id="76b13-112">Виртуальное расположение в сети.</span><span class="sxs-lookup"><span data-stu-id="76b13-112">Virtual network location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b13-113">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="76b13-113">-SubnetId</span></span>
<span data-ttu-id="76b13-114">Имя виртуальной сети, в которую будут развернуты доменные службы.</span><span class="sxs-lookup"><span data-stu-id="76b13-114">The name of the virtual network that Domain Services will be deployed on.</span></span>
<span data-ttu-id="76b13-115">Id подсеть, в которую будут развернуты доменные службы.</span><span class="sxs-lookup"><span data-stu-id="76b13-115">The id of the subnet that Domain Services will be deployed on.</span></span>
<span data-ttu-id="76b13-116">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="76b13-116">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b13-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b13-117">CommonParameters</span></span>
<span data-ttu-id="76b13-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76b13-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76b13-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76b13-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b13-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76b13-120">INPUTS</span></span>

## <span data-ttu-id="76b13-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="76b13-121">OUTPUTS</span></span>

### <span data-ttu-id="76b13-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="76b13-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span></span>

## <span data-ttu-id="76b13-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="76b13-123">NOTES</span></span>

<span data-ttu-id="76b13-124">ALIASES</span><span class="sxs-lookup"><span data-stu-id="76b13-124">ALIASES</span></span>

## <span data-ttu-id="76b13-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76b13-125">RELATED LINKS</span></span>

