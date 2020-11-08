---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseCopy.md
ms.openlocfilehash: e4cfdb8cd7ffc99c3beed66de427af458538bab8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065221"
---
# <span data-ttu-id="0778c-101">New-AzSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="0778c-101">New-AzSqlDatabaseCopy</span></span>

## <span data-ttu-id="0778c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0778c-102">SYNOPSIS</span></span>
<span data-ttu-id="0778c-103">Создает копию базы данных SQL, в которой используется моментальный снимок в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="0778c-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

## <span data-ttu-id="0778c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0778c-104">SYNTAX</span></span>

### <span data-ttu-id="0778c-105">DtuBasedDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0778c-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>] -CopyDatabaseName <String>
 [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0778c-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="0778c-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseCopy [-DatabaseName] <String> [-Tags <Hashtable>] [-CopyResourceGroupName <String>]
 [-CopyServerName <String>] -CopyDatabaseName <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0778c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0778c-107">DESCRIPTION</span></span>
<span data-ttu-id="0778c-108">Командлет **New-AzSqlDatabaseCopy** создает копию базы данных Azure SQL, в которой используется моментальный снимок данных в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="0778c-108">The **New-AzSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="0778c-109">Используйте этот командлет вместо командлета Start-AzSqlDatabaseCopy, чтобы создать единовременно разовую копию базы данных.</span><span class="sxs-lookup"><span data-stu-id="0778c-109">Use this cmdlet instead of the Start-AzSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="0778c-110">Этот командлет возвращает объект **базы данных** копии.</span><span class="sxs-lookup"><span data-stu-id="0778c-110">This cmdlet returns the **Database** object of the copy.</span></span>
<span data-ttu-id="0778c-111">Примечание. Используйте командлет New-AzSqlDatabaseSecondary, чтобы настроить георепликацию для базы данных.</span><span class="sxs-lookup"><span data-stu-id="0778c-111">Note: Use the New-AzSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>
<span data-ttu-id="0778c-112">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="0778c-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0778c-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0778c-113">EXAMPLES</span></span>

## <span data-ttu-id="0778c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0778c-114">PARAMETERS</span></span>

### <span data-ttu-id="0778c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0778c-115">-AsJob</span></span>
<span data-ttu-id="0778c-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0778c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0778c-117">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="0778c-117">-ComputeGeneration</span></span>
<span data-ttu-id="0778c-118">Вычислено поколение, назначаемое новой копии.</span><span class="sxs-lookup"><span data-stu-id="0778c-118">The compute generation to assign to the new copy.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0778c-119">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="0778c-119">-CopyDatabaseName</span></span>
<span data-ttu-id="0778c-120">Указывает имя копии базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="0778c-120">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="0778c-121">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0778c-121">-CopyResourceGroupName</span></span>
<span data-ttu-id="0778c-122">Указывает имя группы ресурсов Azure, в которую нужно назначить копию.</span><span class="sxs-lookup"><span data-stu-id="0778c-122">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="0778c-123">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="0778c-123">-CopyServerName</span></span>
<span data-ttu-id="0778c-124">Указывает имя сервера SQL Server, на котором размещается копия.</span><span class="sxs-lookup"><span data-stu-id="0778c-124">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="0778c-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0778c-125">-DatabaseName</span></span>
<span data-ttu-id="0778c-126">Указывает имя базы данных SQL для копирования.</span><span class="sxs-lookup"><span data-stu-id="0778c-126">Specifies the name of the SQL Database to copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0778c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0778c-127">-DefaultProfile</span></span>
<span data-ttu-id="0778c-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0778c-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0778c-129">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="0778c-129">-ElasticPoolName</span></span>
<span data-ttu-id="0778c-130">Указывает имя эластичного пула, в который нужно назначить копию.</span><span class="sxs-lookup"><span data-stu-id="0778c-130">Specifies the name of the elastic pool in which to assign the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0778c-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0778c-131">-LicenseType</span></span>
<span data-ttu-id="0778c-132">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0778c-132">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="0778c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0778c-133">-ResourceGroupName</span></span>
<span data-ttu-id="0778c-134">Указывает имя группы ресурсов, содержащей базу данных, которую необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="0778c-134">Specifies the name of the Resource Group that contains the database to copy.</span></span>

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

### <span data-ttu-id="0778c-135">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="0778c-135">-ServerName</span></span>
<span data-ttu-id="0778c-136">Указывает имя сервера SQL Server, содержащего базу данных, которую необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="0778c-136">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="0778c-137">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="0778c-137">-ServiceObjectiveName</span></span>
<span data-ttu-id="0778c-138">Указывает имя цели обслуживания, которую нужно назначить копии.</span><span class="sxs-lookup"><span data-stu-id="0778c-138">Specifies the name of the service objective to assign to the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0778c-139">-Теги</span><span class="sxs-lookup"><span data-stu-id="0778c-139">-Tags</span></span>
<span data-ttu-id="0778c-140">Задает пары "ключ-значение" в форме хэш-таблицы, которую нужно связать с копией базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0778c-140">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="0778c-141">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="0778c-141">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0778c-142">-VCore</span><span class="sxs-lookup"><span data-stu-id="0778c-142">-VCore</span></span>
<span data-ttu-id="0778c-143">Vcore номера копий базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0778c-143">The Vcore numbers of the Azure Sql Database copy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0778c-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0778c-144">-Confirm</span></span>
<span data-ttu-id="0778c-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0778c-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0778c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0778c-146">-WhatIf</span></span>
<span data-ttu-id="0778c-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0778c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0778c-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0778c-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0778c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0778c-149">CommonParameters</span></span>
<span data-ttu-id="0778c-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0778c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0778c-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0778c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0778c-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0778c-152">INPUTS</span></span>

### <span data-ttu-id="0778c-153">System. String</span><span class="sxs-lookup"><span data-stu-id="0778c-153">System.String</span></span>

## <span data-ttu-id="0778c-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0778c-154">OUTPUTS</span></span>

### <span data-ttu-id="0778c-155">Microsoft. Azure. Commands. SQL. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="0778c-155">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>

## <span data-ttu-id="0778c-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="0778c-156">NOTES</span></span>

## <span data-ttu-id="0778c-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0778c-157">RELATED LINKS</span></span>

[<span data-ttu-id="0778c-158">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="0778c-158">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="0778c-159">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="0778c-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)