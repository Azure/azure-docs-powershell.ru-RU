---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: a87a11b1e894864593d9558b123b19b6bda06e11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727472"
---
# <span data-ttu-id="f0837-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="f0837-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="f0837-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0837-102">SYNOPSIS</span></span>
<span data-ttu-id="f0837-103">Получение или перечисление узлов.</span><span class="sxs-lookup"><span data-stu-id="f0837-103">Get or list hosts.</span></span>

## <span data-ttu-id="f0837-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0837-104">SYNTAX</span></span>

### <span data-ttu-id="f0837-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0837-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0837-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="f0837-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0837-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0837-107">DESCRIPTION</span></span>
<span data-ttu-id="f0837-108">Этот командлет получит группу узлов.</span><span class="sxs-lookup"><span data-stu-id="f0837-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="f0837-109">Этот командлет также перечисляет все группы узлов в группе ресурсов, если не задано имя группы узлов.</span><span class="sxs-lookup"><span data-stu-id="f0837-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="f0837-110">Этот командлет также перечисляет все группы узлов в подписке, если не заданы ни имя группы узлов, ни имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0837-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="f0837-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0837-111">EXAMPLES</span></span>

### <span data-ttu-id="f0837-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f0837-112">Example 1</span></span>
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

<span data-ttu-id="f0837-113">Эта команда возвращает группу узлов.</span><span class="sxs-lookup"><span data-stu-id="f0837-113">This command returns a host group.</span></span>

### <span data-ttu-id="f0837-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f0837-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="f0837-115">Эта команда возвращает все группы узлов в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0837-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="f0837-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f0837-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="f0837-117">Эта команда возвращает все группы узлов в подписке.</span><span class="sxs-lookup"><span data-stu-id="f0837-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="f0837-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0837-118">PARAMETERS</span></span>

### <span data-ttu-id="f0837-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0837-119">-DefaultProfile</span></span>
<span data-ttu-id="f0837-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0837-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0837-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f0837-121">-Name</span></span>
<span data-ttu-id="f0837-122">Имя группы узлов.</span><span class="sxs-lookup"><span data-stu-id="f0837-122">The name of the host group.</span></span>

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

### <span data-ttu-id="f0837-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0837-123">-ResourceGroupName</span></span>
<span data-ttu-id="f0837-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0837-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="f0837-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0837-125">-ResourceId</span></span>
<span data-ttu-id="f0837-126">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="f0837-126">The ID of the resource.</span></span>

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

### <span data-ttu-id="f0837-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0837-127">CommonParameters</span></span>
<span data-ttu-id="f0837-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0837-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0837-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0837-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0837-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0837-130">INPUTS</span></span>

### <span data-ttu-id="f0837-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f0837-131">System.String</span></span>

## <span data-ttu-id="f0837-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0837-132">OUTPUTS</span></span>

### <span data-ttu-id="f0837-133">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="f0837-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="f0837-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0837-134">NOTES</span></span>

## <span data-ttu-id="f0837-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0837-135">RELATED LINKS</span></span>
