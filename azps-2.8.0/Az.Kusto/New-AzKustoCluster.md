---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: 9157c5dfff46893cfee88d02d8f1564801f889fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720581"
---
# <span data-ttu-id="15681-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="15681-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="15681-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15681-102">SYNOPSIS</span></span>
<span data-ttu-id="15681-103">Создание нового кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="15681-103">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="15681-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15681-104">SYNTAX</span></span>

```
New-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-Tier <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15681-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15681-105">DESCRIPTION</span></span>
<span data-ttu-id="15681-106">Создание нового кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="15681-106">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="15681-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15681-107">EXAMPLES</span></span>

### <span data-ttu-id="15681-108">Пример 1: создание нового кластера Kusto</span><span class="sxs-lookup"><span data-stu-id="15681-108">Example 1 - Create a new Kusto cluster</span></span>

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

<span data-ttu-id="15681-109">В приведенной выше команде создается новый кластер Kusto с именем "mykustocluster" в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="15681-109">The above command creates a new Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="15681-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15681-110">PARAMETERS</span></span>

### <span data-ttu-id="15681-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15681-111">-DefaultProfile</span></span>
<span data-ttu-id="15681-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15681-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15681-113">-Location</span><span class="sxs-lookup"><span data-stu-id="15681-113">-Location</span></span>
<span data-ttu-id="15681-114">Регион Azure, в котором нужно создать кластер.</span><span class="sxs-lookup"><span data-stu-id="15681-114">Azure region where the cluster should be created.</span></span>

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

### <span data-ttu-id="15681-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="15681-115">-Name</span></span>
<span data-ttu-id="15681-116">Имя создаваемого кластера.</span><span class="sxs-lookup"><span data-stu-id="15681-116">Name of the cluster to be created.</span></span>

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

### <span data-ttu-id="15681-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15681-117">-ResourceGroupName</span></span>
<span data-ttu-id="15681-118">Имя группы ресурсов, в которой вы хотите создать кластер.</span><span class="sxs-lookup"><span data-stu-id="15681-118">Name of resource group under which you want to create the cluster.</span></span>

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

### <span data-ttu-id="15681-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="15681-119">-Sku</span></span>
<span data-ttu-id="15681-120">Имя SKU, используемого для создания кластера</span><span class="sxs-lookup"><span data-stu-id="15681-120">Name of the Sku used to create the cluster</span></span>

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

### <span data-ttu-id="15681-121">-Тег</span><span class="sxs-lookup"><span data-stu-id="15681-121">-Tag</span></span>
<span data-ttu-id="15681-122">Строка, словарь строк тегов, связанный с этим кластером</span><span class="sxs-lookup"><span data-stu-id="15681-122">A string,string dictionary of tags associated with this cluster</span></span>

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

### <span data-ttu-id="15681-123">Уровень</span><span class="sxs-lookup"><span data-stu-id="15681-123">-Tier</span></span>
<span data-ttu-id="15681-124">Имя уровня, используемого для создания кластера</span><span class="sxs-lookup"><span data-stu-id="15681-124">Name of the Tier used to create the cluster</span></span>

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

### <span data-ttu-id="15681-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15681-125">-Confirm</span></span>
<span data-ttu-id="15681-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="15681-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15681-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15681-127">-WhatIf</span></span>
<span data-ttu-id="15681-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="15681-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15681-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="15681-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15681-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15681-130">CommonParameters</span></span>
<span data-ttu-id="15681-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15681-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15681-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15681-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15681-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15681-133">INPUTS</span></span>

### <span data-ttu-id="15681-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="15681-134">None</span></span>

## <span data-ttu-id="15681-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15681-135">OUTPUTS</span></span>

### <span data-ttu-id="15681-136">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="15681-136">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="15681-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="15681-137">NOTES</span></span>

## <span data-ttu-id="15681-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15681-138">RELATED LINKS</span></span>
