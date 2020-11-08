---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: 9c18597da52900794e5f891fb06385249c173a0b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065602"
---
# <span data-ttu-id="02799-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="02799-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="02799-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02799-102">SYNOPSIS</span></span>
<span data-ttu-id="02799-103">Создание нового кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="02799-103">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="02799-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02799-104">SYNTAX</span></span>

```
New-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-Tier <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02799-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02799-105">DESCRIPTION</span></span>
<span data-ttu-id="02799-106">Создание нового кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="02799-106">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="02799-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02799-107">EXAMPLES</span></span>

### <span data-ttu-id="02799-108">Пример 1: создание нового кластера Kusto</span><span class="sxs-lookup"><span data-stu-id="02799-108">Example 1 - Create a new Kusto cluster</span></span>

```
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Location 'Central US' -Sku D13_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="02799-109">В приведенной выше команде создается новый кластер Kusto с именем "mykustocluster" в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="02799-109">The above command creates a new Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="02799-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02799-110">PARAMETERS</span></span>

### <span data-ttu-id="02799-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02799-111">-DefaultProfile</span></span>
<span data-ttu-id="02799-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02799-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02799-113">-Location</span><span class="sxs-lookup"><span data-stu-id="02799-113">-Location</span></span>
<span data-ttu-id="02799-114">Регион Azure, в котором нужно создать кластер.</span><span class="sxs-lookup"><span data-stu-id="02799-114">Azure region where the cluster should be created.</span></span>

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

### <span data-ttu-id="02799-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="02799-115">-Name</span></span>
<span data-ttu-id="02799-116">Имя создаваемого кластера.</span><span class="sxs-lookup"><span data-stu-id="02799-116">Name of the cluster to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02799-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02799-117">-ResourceGroupName</span></span>
<span data-ttu-id="02799-118">Имя группы ресурсов, в которой вы хотите создать кластер.</span><span class="sxs-lookup"><span data-stu-id="02799-118">Name of resource group under which you want to create the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02799-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="02799-119">-Sku</span></span>
<span data-ttu-id="02799-120">Имя SKU, используемого для создания кластера</span><span class="sxs-lookup"><span data-stu-id="02799-120">Name of the Sku used to create the cluster</span></span>

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

### <span data-ttu-id="02799-121">-Тег</span><span class="sxs-lookup"><span data-stu-id="02799-121">-Tag</span></span>
<span data-ttu-id="02799-122">Строка, словарь строк тегов, связанный с этим кластером</span><span class="sxs-lookup"><span data-stu-id="02799-122">A string,string dictionary of tags associated with this cluster</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02799-123">Уровень</span><span class="sxs-lookup"><span data-stu-id="02799-123">-Tier</span></span>
<span data-ttu-id="02799-124">Имя уровня, используемого для создания кластера</span><span class="sxs-lookup"><span data-stu-id="02799-124">Name of the Tier used to create the cluster</span></span>

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

### <span data-ttu-id="02799-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02799-125">-Confirm</span></span>
<span data-ttu-id="02799-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="02799-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02799-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02799-127">-WhatIf</span></span>
<span data-ttu-id="02799-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="02799-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02799-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="02799-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02799-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02799-130">CommonParameters</span></span>
<span data-ttu-id="02799-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02799-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02799-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02799-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02799-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02799-133">INPUTS</span></span>

### <span data-ttu-id="02799-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="02799-134">None</span></span>

## <span data-ttu-id="02799-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02799-135">OUTPUTS</span></span>

### <span data-ttu-id="02799-136">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="02799-136">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="02799-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="02799-137">NOTES</span></span>

## <span data-ttu-id="02799-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02799-138">RELATED LINKS</span></span>
