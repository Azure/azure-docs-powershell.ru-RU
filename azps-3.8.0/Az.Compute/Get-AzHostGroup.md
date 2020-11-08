---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: 26030677743b95ebb11431118ccae8adf0b08bcd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073683"
---
# <span data-ttu-id="5a4e8-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="5a4e8-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="5a4e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a4e8-102">SYNOPSIS</span></span>
<span data-ttu-id="5a4e8-103">Получение или перечисление узлов.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-103">Get or list hosts.</span></span>

## <span data-ttu-id="5a4e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a4e8-104">SYNTAX</span></span>

### <span data-ttu-id="5a4e8-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5a4e8-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a4e8-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="5a4e8-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a4e8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a4e8-107">DESCRIPTION</span></span>
<span data-ttu-id="5a4e8-108">Этот командлет получит группу узлов.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="5a4e8-109">Этот командлет также перечисляет все группы узлов в группе ресурсов, если не задано имя группы узлов.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="5a4e8-110">Этот командлет также перечисляет все группы узлов в подписке, если не заданы ни имя группы узлов, ни имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="5a4e8-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a4e8-111">EXAMPLES</span></span>

### <span data-ttu-id="5a4e8-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5a4e8-112">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="5a4e8-113">Эта команда возвращает группу узлов.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-113">This command returns a host group.</span></span>

### <span data-ttu-id="5a4e8-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5a4e8-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="5a4e8-115">Эта команда возвращает все группы узлов в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="5a4e8-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5a4e8-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="5a4e8-117">Эта команда возвращает все группы узлов в подписке.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="5a4e8-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a4e8-118">PARAMETERS</span></span>

### <span data-ttu-id="5a4e8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a4e8-119">-DefaultProfile</span></span>
<span data-ttu-id="5a4e8-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a4e8-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5a4e8-121">-Name</span></span>
<span data-ttu-id="5a4e8-122">Имя группы узлов.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-122">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a4e8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a4e8-123">-ResourceGroupName</span></span>
<span data-ttu-id="5a4e8-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a4e8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a4e8-125">-ResourceId</span></span>
<span data-ttu-id="5a4e8-126">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-126">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a4e8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a4e8-127">CommonParameters</span></span>
<span data-ttu-id="5a4e8-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a4e8-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a4e8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a4e8-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a4e8-130">INPUTS</span></span>

### <span data-ttu-id="5a4e8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5a4e8-131">System.String</span></span>

## <span data-ttu-id="5a4e8-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a4e8-132">OUTPUTS</span></span>

### <span data-ttu-id="5a4e8-133">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="5a4e8-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="5a4e8-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a4e8-134">NOTES</span></span>

## <span data-ttu-id="5a4e8-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a4e8-135">RELATED LINKS</span></span>
