---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 3dbcbed2466f9bb6b229a6dcfa710d6745a72eac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249788"
---
# <span data-ttu-id="8cf64-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8cf64-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="8cf64-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8cf64-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf64-103">Удаление долгосрочной резервной копии хранения.</span><span class="sxs-lookup"><span data-stu-id="8cf64-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="8cf64-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8cf64-104">SYNTAX</span></span>

### <span data-ttu-id="8cf64-105">RemoveBackupDefault (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8cf64-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cf64-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="8cf64-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cf64-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="8cf64-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cf64-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cf64-108">DESCRIPTION</span></span>
<span data-ttu-id="8cf64-109">Командлет **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** удаляет указанную резервную копию.</span><span class="sxs-lookup"><span data-stu-id="8cf64-109">The **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="8cf64-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8cf64-110">EXAMPLES</span></span>

### <span data-ttu-id="8cf64-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8cf64-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

<span data-ttu-id="8cf64-112">Удаление резервной копии с именем 15be823c-7e2c-49d8-819f-a3fdcad92215; 132268250550000000</span><span class="sxs-lookup"><span data-stu-id="8cf64-112">Deletes the backup with name 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span></span>

## <span data-ttu-id="8cf64-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8cf64-113">PARAMETERS</span></span>

### <span data-ttu-id="8cf64-114">-BackupName</span><span class="sxs-lookup"><span data-stu-id="8cf64-114">-BackupName</span></span>
<span data-ttu-id="8cf64-115">Имя резервной копии.</span><span class="sxs-lookup"><span data-stu-id="8cf64-115">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf64-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8cf64-116">-DatabaseName</span></span>
<span data-ttu-id="8cf64-117">Имя управляемой базы данных, из которой находится резервная копия.</span><span class="sxs-lookup"><span data-stu-id="8cf64-117">The name of the Managed Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf64-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf64-118">-DefaultProfile</span></span>
<span data-ttu-id="8cf64-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8cf64-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cf64-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8cf64-120">-Force</span></span>
<span data-ttu-id="8cf64-121">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="8cf64-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="8cf64-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cf64-122">-InputObject</span></span>
<span data-ttu-id="8cf64-123">Удаляемый объект резервного копирования базы данных для хранения.</span><span class="sxs-lookup"><span data-stu-id="8cf64-123">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf64-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="8cf64-124">-InstanceName</span></span>
<span data-ttu-id="8cf64-125">Имя управляемого экземпляра, на котором находится резервная копия.</span><span class="sxs-lookup"><span data-stu-id="8cf64-125">The name of the Managed Instance the backup is under.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf64-126">-Location</span><span class="sxs-lookup"><span data-stu-id="8cf64-126">-Location</span></span>
<span data-ttu-id="8cf64-127">Расположение исходного экземпляра, управляемого с помощью резервных копий.</span><span class="sxs-lookup"><span data-stu-id="8cf64-127">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf64-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cf64-128">-ResourceGroupName</span></span>
<span data-ttu-id="8cf64-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8cf64-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf64-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cf64-130">-ResourceId</span></span>
<span data-ttu-id="8cf64-131">Идентификатор ресурса резервной копии базы данных, для которого необходимо удалить архив.</span><span class="sxs-lookup"><span data-stu-id="8cf64-131">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf64-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cf64-132">-Confirm</span></span>
<span data-ttu-id="8cf64-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8cf64-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cf64-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cf64-134">-WhatIf</span></span>
<span data-ttu-id="8cf64-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8cf64-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cf64-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8cf64-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cf64-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf64-137">CommonParameters</span></span>
<span data-ttu-id="8cf64-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8cf64-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf64-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cf64-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf64-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8cf64-140">INPUTS</span></span>

### <span data-ttu-id="8cf64-141">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="8cf64-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

### <span data-ttu-id="8cf64-142">System. String</span><span class="sxs-lookup"><span data-stu-id="8cf64-142">System.String</span></span>

## <span data-ttu-id="8cf64-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cf64-143">OUTPUTS</span></span>

### <span data-ttu-id="8cf64-144">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="8cf64-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="8cf64-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="8cf64-145">NOTES</span></span>

## <span data-ttu-id="8cf64-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8cf64-146">RELATED LINKS</span></span>

[<span data-ttu-id="8cf64-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8cf64-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="8cf64-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8cf64-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="8cf64-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8cf64-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="8cf64-150">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="8cf64-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)