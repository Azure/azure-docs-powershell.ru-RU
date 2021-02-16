---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Start-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7fe59a6ae103da1fa0ff40bfd300fdbf183fea33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229972"
---
# <span data-ttu-id="e2934-101">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="e2934-101">Start-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="e2934-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2934-102">SYNOPSIS</span></span>
<span data-ttu-id="e2934-103">Запускает службу воспроизведения журнала с заданными параметрами.</span><span class="sxs-lookup"><span data-stu-id="e2934-103">Starts a Log Replay service with the given parameters.</span></span>

## <span data-ttu-id="e2934-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e2934-104">SYNTAX</span></span>

### <span data-ttu-id="e2934-105">LogReplayInstanceDatabaseFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2934-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-AsJob] [-Name] <String>
 [-InstanceName] <String> [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2934-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="e2934-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-AsJob] [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2934-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2934-107">DESCRIPTION</span></span>
<span data-ttu-id="e2934-108">Чтобы запустить службу воспроизведения журнала, запустите начните работу с **start-AzSqlInstanceDatabaseLogReplay.**</span><span class="sxs-lookup"><span data-stu-id="e2934-108">The **Start-AzSqlInstanceDatabaseLogReplay** cmdlet initiate start of the log replay service.</span></span>

## <span data-ttu-id="e2934-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e2934-109">EXAMPLES</span></span>

### <span data-ttu-id="e2934-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e2934-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
    -AutoComplete -LastBackupName "last_backup.bak"
```

<span data-ttu-id="e2934-111">Эта команда создаст новую управляемую базу данных и начнет восстанавливать резервные копии из заданного контейнера, пока last_backup.bak не восстановится.</span><span class="sxs-lookup"><span data-stu-id="e2934-111">This command will create new managed database and will start restoring backups from the given container until last_backup.bak is restored.</span></span>

### <span data-ttu-id="e2934-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e2934-112">Example 2</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
```

<span data-ttu-id="e2934-113">Эта команда создаст новую управляемую базу данных и начнет восстанавливать резервные копии из этого контейнера Complete-AzSqlInstanceDatabaseLogReplay не будет вызван с последней нужной резервной копией.</span><span class="sxs-lookup"><span data-stu-id="e2934-113">This command will create new managed database and will start restoring backups from the given container until Complete-AzSqlInstanceDatabaseLogReplay is called with the last backup wanted.</span></span>

## <span data-ttu-id="e2934-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2934-114">PARAMETERS</span></span>

### <span data-ttu-id="e2934-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2934-115">-AsJob</span></span>
<span data-ttu-id="e2934-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e2934-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2934-117">-AutoCompleteRestore</span><span class="sxs-lookup"><span data-stu-id="e2934-117">-AutoCompleteRestore</span></span>
<span data-ttu-id="e2934-118">Индикатор, следует ли выполнить автоматическое восстановление после завершения.</span><span class="sxs-lookup"><span data-stu-id="e2934-118">The indicator whether or not to auto-complete restore upon completion.</span></span>

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

### <span data-ttu-id="e2934-119">-Collation</span><span class="sxs-lookup"><span data-stu-id="e2934-119">-Collation</span></span>
<span data-ttu-id="e2934-120">Разлиновка используемой базы данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e2934-120">The collation of the instance database to use.</span></span>

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

### <span data-ttu-id="e2934-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2934-121">-DefaultProfile</span></span>
<span data-ttu-id="e2934-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2934-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2934-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2934-123">-InputObject</span></span>
<span data-ttu-id="e2934-124">Объект базы данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e2934-124">The instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2934-125">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e2934-125">-InstanceName</span></span>
<span data-ttu-id="e2934-126">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e2934-126">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2934-127">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="e2934-127">-LastBackupName</span></span>
<span data-ttu-id="e2934-128">Имя последнего файла резервной копии, который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="e2934-128">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="e2934-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e2934-129">-Name</span></span>
<span data-ttu-id="e2934-130">Имя базы данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e2934-130">The name of the instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2934-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2934-131">-PassThru</span></span>
<span data-ttu-id="e2934-132">Определяет, возвращает ли группа синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e2934-132">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="e2934-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2934-133">-ResourceGroupName</span></span>
<span data-ttu-id="e2934-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2934-134">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2934-135">-StorageContainerSasToken</span><span class="sxs-lookup"><span data-stu-id="e2934-135">-StorageContainerSasToken</span></span>
<span data-ttu-id="e2934-136">Маркер Sas контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2934-136">The storage container Sas token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasToken

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2934-137">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="e2934-137">-StorageContainerUri</span></span>
<span data-ttu-id="e2934-138">URI контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2934-138">The storage container URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Storage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2934-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2934-139">-Confirm</span></span>
<span data-ttu-id="e2934-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e2934-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2934-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2934-141">-WhatIf</span></span>
<span data-ttu-id="e2934-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2934-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2934-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e2934-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2934-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2934-144">CommonParameters</span></span>
<span data-ttu-id="e2934-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2934-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2934-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2934-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2934-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2934-147">INPUTS</span></span>

### <span data-ttu-id="e2934-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e2934-148">System.String</span></span>

### <span data-ttu-id="e2934-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e2934-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e2934-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e2934-150">OUTPUTS</span></span>

### <span data-ttu-id="e2934-151">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e2934-151">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e2934-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e2934-152">NOTES</span></span>

## <span data-ttu-id="e2934-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2934-153">RELATED LINKS</span></span>
