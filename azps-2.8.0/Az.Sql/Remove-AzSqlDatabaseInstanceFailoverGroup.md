---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 8027af33b9ea4f4184c10963da69e8be3b4e3961
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906541"
---
# <span data-ttu-id="7fc83-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7fc83-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="7fc83-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7fc83-102">SYNOPSIS</span></span>
<span data-ttu-id="7fc83-103">Удаляет группу отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7fc83-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="7fc83-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7fc83-104">SYNTAX</span></span>

### <span data-ttu-id="7fc83-105">RemoveIFGDefault (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7fc83-105">RemoveIFGDefault (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fc83-106">Удаление группы отработки отказа экземпляра из кода ресурса</span><span class="sxs-lookup"><span data-stu-id="7fc83-106">Remove a Instance Failover Group from Resource Id</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fc83-107">Удаление группы отработки отказа экземпляра из определения экземпляра AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="7fc83-107">Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fc83-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fc83-108">DESCRIPTION</span></span>
<span data-ttu-id="7fc83-109">Эта команда удаляет группу отработки отказа для экземпляра с указанным именем, оставляя все базы данных неизменными.</span><span class="sxs-lookup"><span data-stu-id="7fc83-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="7fc83-110">Конечная точка прослушивателя будет отменена из DNS.</span><span class="sxs-lookup"><span data-stu-id="7fc83-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="7fc83-111">Для выполнения команды следует использовать первичный регион для группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7fc83-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="7fc83-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7fc83-112">EXAMPLES</span></span>

### <span data-ttu-id="7fc83-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7fc83-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="7fc83-114">Удаление группы отработки отказа для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7fc83-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="7fc83-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7fc83-115">PARAMETERS</span></span>

### <span data-ttu-id="7fc83-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fc83-116">-DefaultProfile</span></span>
<span data-ttu-id="7fc83-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7fc83-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fc83-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7fc83-118">-Force</span></span>
<span data-ttu-id="7fc83-119">Пропустить предупреждающее сообщение для выполнения действия.</span><span class="sxs-lookup"><span data-stu-id="7fc83-119">Skip confirmation message for performing the action.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fc83-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fc83-120">-InputObject</span></span>
<span data-ttu-id="7fc83-121">Объект группы для отработки отказа экземпляра, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7fc83-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fc83-122">-Location</span><span class="sxs-lookup"><span data-stu-id="7fc83-122">-Location</span></span>
<span data-ttu-id="7fc83-123">Имя локальной области, из которой извлекается группа отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7fc83-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault, Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fc83-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7fc83-124">-Name</span></span>
<span data-ttu-id="7fc83-125">Имя удаляемой группы отработки отказа для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7fc83-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fc83-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fc83-126">-ResourceGroupName</span></span>
<span data-ttu-id="7fc83-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7fc83-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fc83-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fc83-128">-ResourceId</span></span>
<span data-ttu-id="7fc83-129">Идентификатор ресурса группы отработки отказа для удаления экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7fc83-129">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fc83-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fc83-130">-Confirm</span></span>
<span data-ttu-id="7fc83-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7fc83-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fc83-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fc83-132">-WhatIf</span></span>
<span data-ttu-id="7fc83-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7fc83-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fc83-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7fc83-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fc83-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fc83-135">CommonParameters</span></span>
<span data-ttu-id="7fc83-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7fc83-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fc83-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fc83-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fc83-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7fc83-138">INPUTS</span></span>

### <span data-ttu-id="7fc83-139">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="7fc83-139">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="7fc83-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7fc83-140">System.String</span></span>

## <span data-ttu-id="7fc83-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fc83-141">OUTPUTS</span></span>

### <span data-ttu-id="7fc83-142">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="7fc83-142">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="7fc83-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="7fc83-143">NOTES</span></span>

## <span data-ttu-id="7fc83-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fc83-144">RELATED LINKS</span></span>
