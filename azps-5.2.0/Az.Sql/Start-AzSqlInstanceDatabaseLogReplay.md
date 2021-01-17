---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Start-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 61a87f61efaa889af830cc7bdaa44bcf0b7fc698
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392476"
---
# <span data-ttu-id="c3fb7-101">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="c3fb7-101">Start-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="c3fb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3fb7-102">SYNOPSIS</span></span>
<span data-ttu-id="c3fb7-103">Запускает службу воспроизведения журнала с заданными параметрами.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-103">Starts a Log Replay service with the given parameters.</span></span>

## <span data-ttu-id="c3fb7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c3fb7-104">SYNTAX</span></span>

### <span data-ttu-id="c3fb7-105">LogReplayInstanceDatabaseFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c3fb7-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-Name] <String>
 [-InstanceName] <String> [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3fb7-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="c3fb7-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3fb7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3fb7-107">DESCRIPTION</span></span>
<span data-ttu-id="c3fb7-108">Чтобы запустить службу воспроизведения журнала, запустится **cmdlet Start-AzSqlInstanceDatabaseLogReplay.**</span><span class="sxs-lookup"><span data-stu-id="c3fb7-108">The **Start-AzSqlInstanceDatabaseLogReplay** cmdlet initiate start of the log replay service.</span></span>

## <span data-ttu-id="c3fb7-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c3fb7-109">EXAMPLES</span></span>

### <span data-ttu-id="c3fb7-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c3fb7-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
    -AutoComplete -LastBackupName "last_backup.bak"
```

<span data-ttu-id="c3fb7-111">Эта команда создаст новую управляемую базу данных и начнет восстанавливать резервные копии из заданного контейнера, пока last_backup.bak не восстановится.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-111">This command will create new managed database and will start restoring backups from the given container until last_backup.bak is restored.</span></span>

### <span data-ttu-id="c3fb7-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c3fb7-112">Example 2</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
```

<span data-ttu-id="c3fb7-113">Эта команда создаст новую управляемую базу данных и начнет восстанавливать резервные копии из этого контейнера Complete-AzSqlInstanceDatabaseLogReplay не будет вызван с последней нужной резервной копией.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-113">This command will create new managed database and will start restoring backups from the given container until Complete-AzSqlInstanceDatabaseLogReplay is called with the last backup wanted.</span></span>

## <span data-ttu-id="c3fb7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3fb7-114">PARAMETERS</span></span>

### <span data-ttu-id="c3fb7-115">-AutoCompleteRestore</span><span class="sxs-lookup"><span data-stu-id="c3fb7-115">-AutoCompleteRestore</span></span>
<span data-ttu-id="c3fb7-116">Индикатор, следует ли выполнить автоматическое восстановление после завершения.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-116">The indicator whether or not to auto-complete restore upon completion.</span></span>

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

### <span data-ttu-id="c3fb7-117">-Collation</span><span class="sxs-lookup"><span data-stu-id="c3fb7-117">-Collation</span></span>
<span data-ttu-id="c3fb7-118">Разлиновка используемой базы данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-118">The collation of the instance database to use.</span></span>

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

### <span data-ttu-id="c3fb7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3fb7-119">-DefaultProfile</span></span>
<span data-ttu-id="c3fb7-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3fb7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3fb7-121">-InputObject</span></span>
<span data-ttu-id="c3fb7-122">Объект базы данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-122">The instance database object.</span></span>

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

### <span data-ttu-id="c3fb7-123">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c3fb7-123">-InstanceName</span></span>
<span data-ttu-id="c3fb7-124">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-124">The name of the instance.</span></span>

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

### <span data-ttu-id="c3fb7-125">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="c3fb7-125">-LastBackupName</span></span>
<span data-ttu-id="c3fb7-126">Имя последнего файла резервной копии, который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-126">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="c3fb7-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c3fb7-127">-Name</span></span>
<span data-ttu-id="c3fb7-128">Имя базы данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-128">The name of the instance database.</span></span>

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

### <span data-ttu-id="c3fb7-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3fb7-129">-PassThru</span></span>
<span data-ttu-id="c3fb7-130">Определяет, возвращает ли группа синхронизации.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-130">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="c3fb7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3fb7-131">-ResourceGroupName</span></span>
<span data-ttu-id="c3fb7-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="c3fb7-133">-StorageContainerSasToken</span><span class="sxs-lookup"><span data-stu-id="c3fb7-133">-StorageContainerSasToken</span></span>
<span data-ttu-id="c3fb7-134">Маркер Sas контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-134">The storage container Sas token.</span></span>

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

### <span data-ttu-id="c3fb7-135">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="c3fb7-135">-StorageContainerUri</span></span>
<span data-ttu-id="c3fb7-136">URI контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-136">The storage container URI.</span></span>

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

### <span data-ttu-id="c3fb7-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3fb7-137">-Confirm</span></span>
<span data-ttu-id="c3fb7-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3fb7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3fb7-139">-WhatIf</span></span>
<span data-ttu-id="c3fb7-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3fb7-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3fb7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3fb7-142">CommonParameters</span></span>
<span data-ttu-id="c3fb7-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3fb7-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3fb7-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3fb7-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3fb7-145">INPUTS</span></span>

### <span data-ttu-id="c3fb7-146">System.String</span><span class="sxs-lookup"><span data-stu-id="c3fb7-146">System.String</span></span>

### <span data-ttu-id="c3fb7-147">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="c3fb7-147">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="c3fb7-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c3fb7-148">OUTPUTS</span></span>

### <span data-ttu-id="c3fb7-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="c3fb7-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="c3fb7-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c3fb7-150">NOTES</span></span>

## <span data-ttu-id="c3fb7-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c3fb7-151">RELATED LINKS</span></span>
