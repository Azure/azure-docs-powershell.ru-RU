---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Stop-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 2a7c74c4c8fef61e01ccbbb512ff428b9e885f06
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235761"
---
# <span data-ttu-id="21395-101">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="21395-101">Stop-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="21395-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="21395-102">SYNOPSIS</span></span>
<span data-ttu-id="21395-103">Отменяет службу воспроизведения журнала, удаляя базу данных.</span><span class="sxs-lookup"><span data-stu-id="21395-103">Cancels the Log Replay service by dropping the database.</span></span>

## <span data-ttu-id="21395-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="21395-104">SYNTAX</span></span>

### <span data-ttu-id="21395-105">LogReplayInstanceDatabaseFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="21395-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21395-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="21395-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-PassThru] [-InputObject] <AzureSqlManagedDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21395-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21395-107">DESCRIPTION</span></span>
<span data-ttu-id="21395-108">Командлет **Stop-AzSqlInstanceDatabaseLogReplay** удаляет базу данных и тем самым отменяет службу воспроизведения журнала.</span><span class="sxs-lookup"><span data-stu-id="21395-108">The **Stop-AzSqlInstanceDatabaseLogReplay** cmdlet drops the database and thus cancel Log Replay service.</span></span>

## <span data-ttu-id="21395-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="21395-109">EXAMPLES</span></span>

### <span data-ttu-id="21395-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="21395-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="21395-111">Эта команда будет отменять службу воспроизведения журнала в указанной базе данных.</span><span class="sxs-lookup"><span data-stu-id="21395-111">This command will cancel log replay service on the given database.</span></span>

## <span data-ttu-id="21395-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="21395-112">PARAMETERS</span></span>

### <span data-ttu-id="21395-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21395-113">-DefaultProfile</span></span>
<span data-ttu-id="21395-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="21395-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21395-115">-Force</span><span class="sxs-lookup"><span data-stu-id="21395-115">-Force</span></span>
<span data-ttu-id="21395-116">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="21395-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="21395-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21395-117">-InputObject</span></span>
<span data-ttu-id="21395-118">Объект базы данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="21395-118">The instance database object.</span></span>

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

### <span data-ttu-id="21395-119">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="21395-119">-InstanceName</span></span>
<span data-ttu-id="21395-120">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="21395-120">The name of the instance.</span></span>

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

### <span data-ttu-id="21395-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="21395-121">-Name</span></span>
<span data-ttu-id="21395-122">Имя базы данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="21395-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="21395-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21395-123">-PassThru</span></span>
<span data-ttu-id="21395-124">Определяет, возвращают ли группу синхронизации.</span><span class="sxs-lookup"><span data-stu-id="21395-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="21395-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21395-125">-ResourceGroupName</span></span>
<span data-ttu-id="21395-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="21395-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="21395-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21395-127">-Confirm</span></span>
<span data-ttu-id="21395-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="21395-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21395-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21395-129">-WhatIf</span></span>
<span data-ttu-id="21395-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="21395-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21395-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="21395-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21395-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21395-132">CommonParameters</span></span>
<span data-ttu-id="21395-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="21395-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21395-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21395-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21395-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="21395-135">INPUTS</span></span>

### <span data-ttu-id="21395-136">System. String</span><span class="sxs-lookup"><span data-stu-id="21395-136">System.String</span></span>

### <span data-ttu-id="21395-137">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="21395-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="21395-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="21395-138">OUTPUTS</span></span>

### <span data-ttu-id="21395-139">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="21395-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="21395-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="21395-140">NOTES</span></span>

## <span data-ttu-id="21395-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21395-141">RELATED LINKS</span></span>
