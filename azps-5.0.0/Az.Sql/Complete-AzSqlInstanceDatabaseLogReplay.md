---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: d1d7cead951520944199347ebdbb209c5474eb3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247000"
---
# <span data-ttu-id="1a332-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="1a332-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="1a332-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a332-102">SYNOPSIS</span></span>
<span data-ttu-id="1a332-103">Завершает работу службы воспроизведения журнала для указанной базы данных.</span><span class="sxs-lookup"><span data-stu-id="1a332-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="1a332-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a332-104">SYNTAX</span></span>

### <span data-ttu-id="1a332-105">LogReplayInstanceDatabaseFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1a332-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a332-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="1a332-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a332-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a332-107">DESCRIPTION</span></span>
<span data-ttu-id="1a332-108">Командлет **Complete-AzSqlInstanceDatabaseLogReplay** завершает работу службы воспроизведения журнала в заданной базе данных.</span><span class="sxs-lookup"><span data-stu-id="1a332-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="1a332-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a332-109">EXAMPLES</span></span>

### <span data-ttu-id="1a332-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1a332-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="1a332-111">Эта команда завершает работу службы преобразования журнала для указанной базы данных после восстановления последней резервной копии.</span><span class="sxs-lookup"><span data-stu-id="1a332-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="1a332-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a332-112">PARAMETERS</span></span>

### <span data-ttu-id="1a332-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a332-113">-DefaultProfile</span></span>
<span data-ttu-id="1a332-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a332-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a332-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a332-115">-InputObject</span></span>
<span data-ttu-id="1a332-116">Объект базы данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1a332-116">The instance database object.</span></span>

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

### <span data-ttu-id="1a332-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="1a332-117">-InstanceName</span></span>
<span data-ttu-id="1a332-118">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1a332-118">The name of the instance.</span></span>

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

### <span data-ttu-id="1a332-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="1a332-119">-LastBackupName</span></span>
<span data-ttu-id="1a332-120">Имя последнего файла резервной копии для восстановления.</span><span class="sxs-lookup"><span data-stu-id="1a332-120">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="1a332-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1a332-121">-Name</span></span>
<span data-ttu-id="1a332-122">Имя базы данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1a332-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="1a332-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a332-123">-PassThru</span></span>
<span data-ttu-id="1a332-124">Определяет, возвращают ли группу синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1a332-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="1a332-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a332-125">-ResourceGroupName</span></span>
<span data-ttu-id="1a332-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a332-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="1a332-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a332-127">-Confirm</span></span>
<span data-ttu-id="1a332-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1a332-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a332-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a332-129">-WhatIf</span></span>
<span data-ttu-id="1a332-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1a332-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a332-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1a332-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a332-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a332-132">CommonParameters</span></span>
<span data-ttu-id="1a332-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a332-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a332-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a332-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a332-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a332-135">INPUTS</span></span>

### <span data-ttu-id="1a332-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1a332-136">System.String</span></span>

### <span data-ttu-id="1a332-137">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="1a332-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="1a332-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a332-138">OUTPUTS</span></span>

## <span data-ttu-id="1a332-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a332-139">NOTES</span></span>

## <span data-ttu-id="1a332-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a332-140">RELATED LINKS</span></span>
