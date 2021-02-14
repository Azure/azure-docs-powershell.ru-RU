---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.ADDomainServices/new-AzADDomainServiceReplicaSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
ms.openlocfilehash: f95c4148afa3f317914dabe968376e0e86913dcb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210660"
---
# <span data-ttu-id="1c60b-101">New-AzADDomainServiceReplicaSet</span><span class="sxs-lookup"><span data-stu-id="1c60b-101">New-AzADDomainServiceReplicaSet</span></span>

## <span data-ttu-id="1c60b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c60b-102">SYNOPSIS</span></span>
<span data-ttu-id="1c60b-103">Создание объекта в памяти для ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="1c60b-103">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="1c60b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1c60b-104">SYNTAX</span></span>

```
New-AzADDomainServiceReplicaSet [-Location <String>] [-SubnetId <String>] [<CommonParameters>]
```

## <span data-ttu-id="1c60b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c60b-105">DESCRIPTION</span></span>
<span data-ttu-id="1c60b-106">Создание в памяти объекта для ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="1c60b-106">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="1c60b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1c60b-107">EXAMPLES</span></span>

### <span data-ttu-id="1c60b-108">Пример 1. Создание репликации для AdDomain</span><span class="sxs-lookup"><span data-stu-id="1c60b-108">Example 1: Create ReplicaSet for AdDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceReplicaSet -Location eastus -SubnetId /subscriptions/**********-****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/Microsoft.Network/virtualNetworks/yourinttest/subnets/default

DomainControllerIPAddress ExternalAccessIPAddress HealthLastEvaluated Location ServiceStatus SubnetId
------------------------- ----------------------- ------------------- -------- ------------- --------
                                                                      eastus                 /subscriptions/****
                                                                      ****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/M…
```

<span data-ttu-id="1c60b-109">Create ReplicaSet для AdDomain</span><span class="sxs-lookup"><span data-stu-id="1c60b-109">Create ReplicaSet for AdDomain</span></span>

## <span data-ttu-id="1c60b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c60b-110">PARAMETERS</span></span>

### <span data-ttu-id="1c60b-111">-Location</span><span class="sxs-lookup"><span data-stu-id="1c60b-111">-Location</span></span>
<span data-ttu-id="1c60b-112">Виртуальное расположение в сети.</span><span class="sxs-lookup"><span data-stu-id="1c60b-112">Virtual network location.</span></span>

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

### <span data-ttu-id="1c60b-113">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1c60b-113">-SubnetId</span></span>
<span data-ttu-id="1c60b-114">Имя виртуальной сети, в которую будут развернуты доменные службы.</span><span class="sxs-lookup"><span data-stu-id="1c60b-114">The name of the virtual network that Domain Services will be deployed on.</span></span>
<span data-ttu-id="1c60b-115">Id подсеть, в которую будут развернуты доменные службы.</span><span class="sxs-lookup"><span data-stu-id="1c60b-115">The id of the subnet that Domain Services will be deployed on.</span></span>
<span data-ttu-id="1c60b-116">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="1c60b-116">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

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

### <span data-ttu-id="1c60b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c60b-117">CommonParameters</span></span>
<span data-ttu-id="1c60b-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c60b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c60b-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c60b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c60b-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c60b-120">INPUTS</span></span>

## <span data-ttu-id="1c60b-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1c60b-121">OUTPUTS</span></span>

### <span data-ttu-id="1c60b-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="1c60b-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span></span>

## <span data-ttu-id="1c60b-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1c60b-123">NOTES</span></span>

<span data-ttu-id="1c60b-124">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1c60b-124">ALIASES</span></span>

## <span data-ttu-id="1c60b-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c60b-125">RELATED LINKS</span></span>

