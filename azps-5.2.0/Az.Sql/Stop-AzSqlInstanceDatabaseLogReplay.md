---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Stop-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 2a7c74c4c8fef61e01ccbbb512ff428b9e885f06
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401852"
---
# <span data-ttu-id="7082e-101">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="7082e-101">Stop-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="7082e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7082e-102">SYNOPSIS</span></span>
<span data-ttu-id="7082e-103">Отменяет службу воспроизведения журнала, переоценив базу данных.</span><span class="sxs-lookup"><span data-stu-id="7082e-103">Cancels the Log Replay service by dropping the database.</span></span>

## <span data-ttu-id="7082e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7082e-104">SYNTAX</span></span>

### <span data-ttu-id="7082e-105">LogReplayInstanceDatabaseFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7082e-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7082e-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="7082e-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-PassThru] [-InputObject] <AzureSqlManagedDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7082e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7082e-107">DESCRIPTION</span></span>
<span data-ttu-id="7082e-108">**Cmdlet Stop-AzSqlInstanceDatabaseLogReplay** отбрасняет базу данных и тем самым отменяет службу воспроизведения журнала.</span><span class="sxs-lookup"><span data-stu-id="7082e-108">The **Stop-AzSqlInstanceDatabaseLogReplay** cmdlet drops the database and thus cancel Log Replay service.</span></span>

## <span data-ttu-id="7082e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7082e-109">EXAMPLES</span></span>

### <span data-ttu-id="7082e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7082e-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="7082e-111">Эта команда отменяет службу воспроизведения журнала в данной базе данных.</span><span class="sxs-lookup"><span data-stu-id="7082e-111">This command will cancel log replay service on the given database.</span></span>

## <span data-ttu-id="7082e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7082e-112">PARAMETERS</span></span>

### <span data-ttu-id="7082e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7082e-113">-DefaultProfile</span></span>
<span data-ttu-id="7082e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7082e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7082e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7082e-115">-Force</span></span>
<span data-ttu-id="7082e-116">Пропустить сообщение с подтверждением выполнения действия</span><span class="sxs-lookup"><span data-stu-id="7082e-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="7082e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7082e-117">-InputObject</span></span>
<span data-ttu-id="7082e-118">Объект базы данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7082e-118">The instance database object.</span></span>

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

### <span data-ttu-id="7082e-119">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7082e-119">-InstanceName</span></span>
<span data-ttu-id="7082e-120">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7082e-120">The name of the instance.</span></span>

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

### <span data-ttu-id="7082e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7082e-121">-Name</span></span>
<span data-ttu-id="7082e-122">Имя базы данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7082e-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="7082e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7082e-123">-PassThru</span></span>
<span data-ttu-id="7082e-124">Определяет, возвращает ли группа синхронизации.</span><span class="sxs-lookup"><span data-stu-id="7082e-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="7082e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7082e-125">-ResourceGroupName</span></span>
<span data-ttu-id="7082e-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7082e-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="7082e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7082e-127">-Confirm</span></span>
<span data-ttu-id="7082e-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7082e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7082e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7082e-129">-WhatIf</span></span>
<span data-ttu-id="7082e-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7082e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7082e-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7082e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7082e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7082e-132">CommonParameters</span></span>
<span data-ttu-id="7082e-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7082e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7082e-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7082e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7082e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7082e-135">INPUTS</span></span>

### <span data-ttu-id="7082e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7082e-136">System.String</span></span>

### <span data-ttu-id="7082e-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7082e-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="7082e-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7082e-138">OUTPUTS</span></span>

### <span data-ttu-id="7082e-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7082e-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="7082e-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7082e-140">NOTES</span></span>

## <span data-ttu-id="7082e-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7082e-141">RELATED LINKS</span></span>
