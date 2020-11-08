---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: 47b519b324018e4fc369d281f7fb7eac554ac571
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065597"
---
# <span data-ttu-id="ecbfc-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="ecbfc-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="ecbfc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ecbfc-102">SYNOPSIS</span></span>
<span data-ttu-id="ecbfc-103">Удаляет существующую базу данных Kusto.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-103">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="ecbfc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ecbfc-104">SYNTAX</span></span>

### <span data-ttu-id="ecbfc-105">ByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ecbfc-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecbfc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ecbfc-106">ByResourceId</span></span>
```
Remove-AzKustoDatabase [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecbfc-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ecbfc-107">ByInputObject</span></span>
```
Remove-AzKustoDatabase [-InputObject] <PSKustoDatabase> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecbfc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecbfc-108">DESCRIPTION</span></span>
<span data-ttu-id="ecbfc-109">Удаляет существующую базу данных Kusto.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-109">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="ecbfc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ecbfc-110">EXAMPLES</span></span>

### <span data-ttu-id="ecbfc-111">Пример 1: удаление существующей базы данных Kusto по имени</span><span class="sxs-lookup"><span data-stu-id="ecbfc-111">Example 1 - Delete an existing Kusto database by name</span></span>

```
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase
```

<span data-ttu-id="ecbfc-112">Вышеприведенная команда удаляет базу данных Kusto с именем "mykustodatabase" в кластере "mykustocluster", обнаруженную в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="ecbfc-112">The above command deletes the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="ecbfc-113">Пример 2. Удаление существующей базы данных Kusto с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="ecbfc-113">Example 2 - Delete an existing Kusto database by piping</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Remove-AzKustoDatabase
```

<span data-ttu-id="ecbfc-114">Вышеприведенная команда получает базу данных Kusto с именем "mykustodatabase" в кластере "mykustocluster", обнаруженную в группе ресурсов "testrg" с помощью `Get-AzKustoDatabase` командлета, а затем `Remove-AzKustoDatabase` передается результат, чтобы удалить его.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-114">The above command gets the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Remove-AzKustoDatabase` to delete it.</span></span>

## <span data-ttu-id="ecbfc-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ecbfc-115">PARAMETERS</span></span>

### <span data-ttu-id="ecbfc-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="ecbfc-116">-ClusterName</span></span>
<span data-ttu-id="ecbfc-117">Имя кластера, в котором находится база данных.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-117">Name of the cluster under which the database exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecbfc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecbfc-118">-DefaultProfile</span></span>
<span data-ttu-id="ecbfc-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecbfc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecbfc-120">-InputObject</span></span>
<span data-ttu-id="ecbfc-121">Объект базы данных Kusto.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-121">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecbfc-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ecbfc-122">-Name</span></span>
<span data-ttu-id="ecbfc-123">Имя базы данных, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-123">Name of database to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecbfc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecbfc-124">-PassThru</span></span>
<span data-ttu-id="ecbfc-125">Возвращают данные о том, была ли база данных успешно приостановлена или нет.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-125">Return whether the specified database was successfully suspended or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecbfc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecbfc-126">-ResourceGroupName</span></span>
<span data-ttu-id="ecbfc-127">Имя группы ресурсов, в которой находится кластер.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-127">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecbfc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecbfc-128">-ResourceId</span></span>
<span data-ttu-id="ecbfc-129">ИД ресурса Kusto базы данных.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-129">Kusto database ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecbfc-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecbfc-130">-Confirm</span></span>
<span data-ttu-id="ecbfc-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecbfc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecbfc-132">-WhatIf</span></span>
<span data-ttu-id="ecbfc-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecbfc-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecbfc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecbfc-135">CommonParameters</span></span>
<span data-ttu-id="ecbfc-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecbfc-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecbfc-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecbfc-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ecbfc-138">INPUTS</span></span>

### <span data-ttu-id="ecbfc-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ecbfc-139">System.String</span></span>

### <span data-ttu-id="ecbfc-140">Microsoft. Azure. Commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="ecbfc-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="ecbfc-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecbfc-141">OUTPUTS</span></span>

### <span data-ttu-id="ecbfc-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ecbfc-142">System.Boolean</span></span>

## <span data-ttu-id="ecbfc-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="ecbfc-143">NOTES</span></span>

## <span data-ttu-id="ecbfc-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ecbfc-144">RELATED LINKS</span></span>
