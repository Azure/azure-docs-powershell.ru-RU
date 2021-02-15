---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: e5cd2c2e6e903afd5afeafe2ca5fcdc70551e582
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235532"
---
# <span data-ttu-id="52bc9-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="52bc9-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="52bc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="52bc9-103">Отбой для базы данных.</span><span class="sxs-lookup"><span data-stu-id="52bc9-103">Failovers a database.</span></span>

## <span data-ttu-id="52bc9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="52bc9-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52bc9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52bc9-105">DESCRIPTION</span></span>
<span data-ttu-id="52bc9-106">От Invoke-AzSqlDatabaseFailover отбойного управления для SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="52bc9-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="52bc9-107">Если база данных находится в эластичном пуле, эта команда отополномет данную базу данных, не влияя на другие базы данных в этом же пуле.</span><span class="sxs-lookup"><span data-stu-id="52bc9-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="52bc9-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="52bc9-108">EXAMPLES</span></span>

### <span data-ttu-id="52bc9-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="52bc9-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="52bc9-110">Эта команда отзовет основную копию базы данных Database01 на сервере с именем "Сервер01".</span><span class="sxs-lookup"><span data-stu-id="52bc9-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="52bc9-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="52bc9-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="52bc9-112">Эта команда отобразит учитаемую вторичную копию базы данных "Database01" на сервере с именем "Сервер01".</span><span class="sxs-lookup"><span data-stu-id="52bc9-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="52bc9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52bc9-113">PARAMETERS</span></span>

### <span data-ttu-id="52bc9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52bc9-114">-AsJob</span></span>
<span data-ttu-id="52bc9-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="52bc9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52bc9-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="52bc9-116">-DatabaseName</span></span>
<span data-ttu-id="52bc9-117">Имя базы данных Azure SQL отбой.</span><span class="sxs-lookup"><span data-stu-id="52bc9-117">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="52bc9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52bc9-118">-DefaultProfile</span></span>
<span data-ttu-id="52bc9-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52bc9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52bc9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="52bc9-120">-Force</span></span>
<span data-ttu-id="52bc9-121">Пропустить сообщение с подтверждением выполнения действия</span><span class="sxs-lookup"><span data-stu-id="52bc9-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="52bc9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52bc9-122">-PassThru</span></span>
<span data-ttu-id="52bc9-123">При успешном выполнении возвращается истина.</span><span class="sxs-lookup"><span data-stu-id="52bc9-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="52bc9-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="52bc9-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="52bc9-125">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="52bc9-125">-ReadableSecondary</span></span>
<span data-ttu-id="52bc9-126">Отбой для учитаемой вторичной реплики вместо основной реплики по умолчанию</span><span class="sxs-lookup"><span data-stu-id="52bc9-126">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="52bc9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52bc9-127">-ResourceGroupName</span></span>
<span data-ttu-id="52bc9-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="52bc9-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="52bc9-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="52bc9-129">-ServerName</span></span>
<span data-ttu-id="52bc9-130">Имя сервера баз данных Azure SQL, в которой находится база данных.</span><span class="sxs-lookup"><span data-stu-id="52bc9-130">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="52bc9-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52bc9-131">-Confirm</span></span>
<span data-ttu-id="52bc9-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52bc9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52bc9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52bc9-133">-WhatIf</span></span>
<span data-ttu-id="52bc9-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52bc9-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52bc9-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="52bc9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52bc9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52bc9-136">CommonParameters</span></span>
<span data-ttu-id="52bc9-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52bc9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52bc9-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52bc9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52bc9-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52bc9-139">INPUTS</span></span>

### <span data-ttu-id="52bc9-140">System.String</span><span class="sxs-lookup"><span data-stu-id="52bc9-140">System.String</span></span>

## <span data-ttu-id="52bc9-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="52bc9-141">OUTPUTS</span></span>

## <span data-ttu-id="52bc9-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="52bc9-142">NOTES</span></span>

## <span data-ttu-id="52bc9-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52bc9-143">RELATED LINKS</span></span>

[<span data-ttu-id="52bc9-144">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="52bc9-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="52bc9-145">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="52bc9-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="52bc9-146">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="52bc9-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="52bc9-147">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="52bc9-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="52bc9-148">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="52bc9-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="52bc9-149">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="52bc9-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="52bc9-150">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="52bc9-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="52bc9-151">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="52bc9-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
