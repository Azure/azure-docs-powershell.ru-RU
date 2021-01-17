---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 3dbcbed2466f9bb6b229a6dcfa710d6745a72eac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419092"
---
# <span data-ttu-id="3c1e4-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="3c1e4-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="3c1e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c1e4-102">SYNOPSIS</span></span>
<span data-ttu-id="3c1e4-103">Удаляет резервную копию хранения в течение длительного времени.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="3c1e4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3c1e4-104">SYNTAX</span></span>

### <span data-ttu-id="3c1e4-105">RemoveBackupDefault (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3c1e4-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c1e4-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="3c1e4-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c1e4-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="3c1e4-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c1e4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c1e4-108">DESCRIPTION</span></span>
<span data-ttu-id="3c1e4-109">Для удаления указанной резервной копии будет удалена указанная резервная копия, указанный при наступлении **azSqlInstanceDatabaseLongTermRetentionBackup.**</span><span class="sxs-lookup"><span data-stu-id="3c1e4-109">The **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="3c1e4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3c1e4-110">EXAMPLES</span></span>

### <span data-ttu-id="3c1e4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3c1e4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

<span data-ttu-id="3c1e4-112">Удаляет резервную копию с именем 15be823c-7e2c-49d8-819f-a3fdcad92215;13226825055000000</span><span class="sxs-lookup"><span data-stu-id="3c1e4-112">Deletes the backup with name 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span></span>

## <span data-ttu-id="3c1e4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c1e4-113">PARAMETERS</span></span>

### <span data-ttu-id="3c1e4-114">-BackupName</span><span class="sxs-lookup"><span data-stu-id="3c1e4-114">-BackupName</span></span>
<span data-ttu-id="3c1e4-115">Имя резервной копии.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-115">The name of the backup.</span></span>

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

### <span data-ttu-id="3c1e4-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3c1e4-116">-DatabaseName</span></span>
<span data-ttu-id="3c1e4-117">Имя управляемой базы данных, из которой создана резервная копия.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-117">The name of the Managed Database the backup is from.</span></span>

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

### <span data-ttu-id="3c1e4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c1e4-118">-DefaultProfile</span></span>
<span data-ttu-id="3c1e4-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c1e4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3c1e4-120">-Force</span></span>
<span data-ttu-id="3c1e4-121">Пропустить сообщение с подтверждением выполнения действия</span><span class="sxs-lookup"><span data-stu-id="3c1e4-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3c1e4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c1e4-122">-InputObject</span></span>
<span data-ttu-id="3c1e4-123">Объект долгосрочной резервной копии базы данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-123">The Database Long Term Retention Backup object to remove.</span></span>

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

### <span data-ttu-id="3c1e4-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3c1e4-124">-InstanceName</span></span>
<span data-ttu-id="3c1e4-125">Имя управляемого экземпляра, под которым находится резервная копия.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-125">The name of the Managed Instance the backup is under.</span></span>

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

### <span data-ttu-id="3c1e4-126">-Location</span><span class="sxs-lookup"><span data-stu-id="3c1e4-126">-Location</span></span>
<span data-ttu-id="3c1e4-127">Расположение управляемого экземпляра резервной копии.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-127">The location of the backups' source Managed Instance.</span></span>

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

### <span data-ttu-id="3c1e4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c1e4-128">-ResourceGroupName</span></span>
<span data-ttu-id="3c1e4-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="3c1e4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c1e4-130">-ResourceId</span></span>
<span data-ttu-id="3c1e4-131">Код ресурса базы данных, из которой нужно удалить резервную копию данных в течение долгого времени.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-131">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

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

### <span data-ttu-id="3c1e4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c1e4-132">-Confirm</span></span>
<span data-ttu-id="3c1e4-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c1e4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c1e4-134">-WhatIf</span></span>
<span data-ttu-id="3c1e4-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c1e4-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c1e4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c1e4-137">CommonParameters</span></span>
<span data-ttu-id="3c1e4-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c1e4-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c1e4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c1e4-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c1e4-140">INPUTS</span></span>

### <span data-ttu-id="3c1e4-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="3c1e4-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

### <span data-ttu-id="3c1e4-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3c1e4-142">System.String</span></span>

## <span data-ttu-id="3c1e4-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3c1e4-143">OUTPUTS</span></span>

### <span data-ttu-id="3c1e4-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="3c1e4-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="3c1e4-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3c1e4-145">NOTES</span></span>

## <span data-ttu-id="3c1e4-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c1e4-146">RELATED LINKS</span></span>

[<span data-ttu-id="3c1e4-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="3c1e4-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="3c1e4-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3c1e4-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="3c1e4-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3c1e4-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="3c1e4-150">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="3c1e4-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)