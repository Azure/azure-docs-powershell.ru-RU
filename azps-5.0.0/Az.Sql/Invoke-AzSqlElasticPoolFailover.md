---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: 631a8edcc3709e80b36a3ff8661b7ea6027b9f78
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245660"
---
# <span data-ttu-id="33b3e-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="33b3e-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="33b3e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="33b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="33b3e-103">Отработка отказа эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="33b3e-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="33b3e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="33b3e-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33b3e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33b3e-105">DESCRIPTION</span></span>
<span data-ttu-id="33b3e-106">Командлет Invoke-AzSqlElasticPoolFailover отработка отказа эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="33b3e-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="33b3e-107">Отработка отказа выполняется для всех баз данных в пуле эластичных БД после выполнения этого командлета.</span><span class="sxs-lookup"><span data-stu-id="33b3e-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="33b3e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="33b3e-108">EXAMPLES</span></span>

### <span data-ttu-id="33b3e-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="33b3e-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="33b3e-110">Эта команда будет отработка отказа для пула эластичных БД с именем "ElasticPool01" на сервере с именем "Server01".</span><span class="sxs-lookup"><span data-stu-id="33b3e-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="33b3e-111">Это означает, что переход на другой ресурс выполняется для всех баз данных в пуле эластичных БД с именем "ElasticPool01".</span><span class="sxs-lookup"><span data-stu-id="33b3e-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="33b3e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="33b3e-112">PARAMETERS</span></span>

### <span data-ttu-id="33b3e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33b3e-113">-AsJob</span></span>
<span data-ttu-id="33b3e-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="33b3e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33b3e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33b3e-115">-DefaultProfile</span></span>
<span data-ttu-id="33b3e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="33b3e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33b3e-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="33b3e-117">-ElasticPoolName</span></span>
<span data-ttu-id="33b3e-118">Имя пула эластичных БД SQL для Azure, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="33b3e-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b3e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="33b3e-119">-Force</span></span>
<span data-ttu-id="33b3e-120">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="33b3e-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="33b3e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33b3e-121">-PassThru</span></span>
<span data-ttu-id="33b3e-122">При успешном выполнении возвращает значение истина.</span><span class="sxs-lookup"><span data-stu-id="33b3e-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="33b3e-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="33b3e-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="33b3e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33b3e-124">-ResourceGroupName</span></span>
<span data-ttu-id="33b3e-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="33b3e-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b3e-126">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="33b3e-126">-ServerName</span></span>
<span data-ttu-id="33b3e-127">Имя сервера Azure SQL Server, в котором находится пул эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="33b3e-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b3e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33b3e-128">-Confirm</span></span>
<span data-ttu-id="33b3e-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="33b3e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33b3e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33b3e-130">-WhatIf</span></span>
<span data-ttu-id="33b3e-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="33b3e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33b3e-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="33b3e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33b3e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33b3e-133">CommonParameters</span></span>
<span data-ttu-id="33b3e-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="33b3e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33b3e-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33b3e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33b3e-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="33b3e-136">INPUTS</span></span>

### <span data-ttu-id="33b3e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="33b3e-137">System.String</span></span>

## <span data-ttu-id="33b3e-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33b3e-138">OUTPUTS</span></span>

## <span data-ttu-id="33b3e-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="33b3e-139">NOTES</span></span>

## <span data-ttu-id="33b3e-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33b3e-140">RELATED LINKS</span></span>

[<span data-ttu-id="33b3e-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="33b3e-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="33b3e-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="33b3e-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="33b3e-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="33b3e-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="33b3e-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="33b3e-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="33b3e-145">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="33b3e-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="33b3e-146">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="33b3e-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="33b3e-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="33b3e-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="33b3e-148">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="33b3e-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)