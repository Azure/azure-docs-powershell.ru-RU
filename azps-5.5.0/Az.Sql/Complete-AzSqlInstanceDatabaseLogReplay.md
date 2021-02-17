---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: d1d7cead951520944199347ebdbb209c5474eb3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230321"
---
# <span data-ttu-id="eb244-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="eb244-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="eb244-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb244-102">SYNOPSIS</span></span>
<span data-ttu-id="eb244-103">Завершение работы службы воспроизведения журнала для данной базы данных.</span><span class="sxs-lookup"><span data-stu-id="eb244-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="eb244-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eb244-104">SYNTAX</span></span>

### <span data-ttu-id="eb244-105">LogReplayInstanceDatabaseFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eb244-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb244-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="eb244-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb244-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb244-107">DESCRIPTION</span></span>
<span data-ttu-id="eb244-108">**Полный-AzSqlInstanceDatabaseLogReplay** завершает службу воспроизведения журнала в данной базе данных.</span><span class="sxs-lookup"><span data-stu-id="eb244-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="eb244-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eb244-109">EXAMPLES</span></span>

### <span data-ttu-id="eb244-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eb244-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="eb244-111">Эта команда завершит службу воспроизведения журнала для данной базы данных после восстановления последней резервной копии.</span><span class="sxs-lookup"><span data-stu-id="eb244-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="eb244-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb244-112">PARAMETERS</span></span>

### <span data-ttu-id="eb244-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb244-113">-DefaultProfile</span></span>
<span data-ttu-id="eb244-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb244-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb244-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb244-115">-InputObject</span></span>
<span data-ttu-id="eb244-116">Объект базы данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="eb244-116">The instance database object.</span></span>

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

### <span data-ttu-id="eb244-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="eb244-117">-InstanceName</span></span>
<span data-ttu-id="eb244-118">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="eb244-118">The name of the instance.</span></span>

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

### <span data-ttu-id="eb244-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="eb244-119">-LastBackupName</span></span>
<span data-ttu-id="eb244-120">Имя последнего файла резервной копии, который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="eb244-120">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="eb244-121">-Name</span><span class="sxs-lookup"><span data-stu-id="eb244-121">-Name</span></span>
<span data-ttu-id="eb244-122">Имя базы данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="eb244-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="eb244-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb244-123">-PassThru</span></span>
<span data-ttu-id="eb244-124">Определяет, возвращает ли группа синхронизации.</span><span class="sxs-lookup"><span data-stu-id="eb244-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="eb244-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb244-125">-ResourceGroupName</span></span>
<span data-ttu-id="eb244-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eb244-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="eb244-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb244-127">-Confirm</span></span>
<span data-ttu-id="eb244-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="eb244-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb244-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb244-129">-WhatIf</span></span>
<span data-ttu-id="eb244-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb244-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb244-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="eb244-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb244-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb244-132">CommonParameters</span></span>
<span data-ttu-id="eb244-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb244-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb244-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb244-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb244-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb244-135">INPUTS</span></span>

### <span data-ttu-id="eb244-136">System.String</span><span class="sxs-lookup"><span data-stu-id="eb244-136">System.String</span></span>

### <span data-ttu-id="eb244-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="eb244-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="eb244-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eb244-138">OUTPUTS</span></span>

## <span data-ttu-id="eb244-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eb244-139">NOTES</span></span>

## <span data-ttu-id="eb244-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb244-140">RELATED LINKS</span></span>
