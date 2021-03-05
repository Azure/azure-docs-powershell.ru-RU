---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: ce69f6b087a7ed61f415e3d6a649f757bb10178f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995095"
---
# <span data-ttu-id="bdc01-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="bdc01-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="bdc01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdc01-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc01-103">Удаляет группу синхронизации баз SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bdc01-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="bdc01-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bdc01-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bdc01-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdc01-105">DESCRIPTION</span></span>
<span data-ttu-id="bdc01-106">При этом удаляется группа синхронизации базы данных Azure SQL **AzSqlSyncGroup.**</span><span class="sxs-lookup"><span data-stu-id="bdc01-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="bdc01-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bdc01-107">EXAMPLES</span></span>

### <span data-ttu-id="bdc01-108">Пример 1. Удаление группы синхронизации</span><span class="sxs-lookup"><span data-stu-id="bdc01-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="bdc01-109">Эта команда удаляет группу синхронизации баз данных Azure SQL с именем syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="bdc01-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="bdc01-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdc01-110">PARAMETERS</span></span>

### <span data-ttu-id="bdc01-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bdc01-111">-DatabaseName</span></span>
<span data-ttu-id="bdc01-112">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="bdc01-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="bdc01-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc01-113">-DefaultProfile</span></span>
<span data-ttu-id="bdc01-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bdc01-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdc01-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bdc01-115">-Force</span></span>
<span data-ttu-id="bdc01-116">Пропустить сообщение с подтверждением выполнения действия</span><span class="sxs-lookup"><span data-stu-id="bdc01-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="bdc01-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bdc01-117">-Name</span></span>
<span data-ttu-id="bdc01-118">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="bdc01-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdc01-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bdc01-119">-PassThru</span></span>
<span data-ttu-id="bdc01-120">Определяет, возвращает ли удаленная группа синхронизации</span><span class="sxs-lookup"><span data-stu-id="bdc01-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="bdc01-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdc01-121">-ResourceGroupName</span></span>
<span data-ttu-id="bdc01-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bdc01-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="bdc01-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bdc01-123">-ServerName</span></span>
<span data-ttu-id="bdc01-124">Имя службы Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bdc01-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="bdc01-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bdc01-125">-Confirm</span></span>
<span data-ttu-id="bdc01-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bdc01-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdc01-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdc01-127">-WhatIf</span></span>
<span data-ttu-id="bdc01-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdc01-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdc01-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bdc01-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdc01-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc01-130">CommonParameters</span></span>
<span data-ttu-id="bdc01-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdc01-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc01-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bdc01-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc01-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bdc01-133">INPUTS</span></span>

### <span data-ttu-id="bdc01-134">System.String</span><span class="sxs-lookup"><span data-stu-id="bdc01-134">System.String</span></span>

## <span data-ttu-id="bdc01-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bdc01-135">OUTPUTS</span></span>

### <span data-ttu-id="bdc01-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="bdc01-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="bdc01-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bdc01-137">NOTES</span></span>

## <span data-ttu-id="bdc01-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bdc01-138">RELATED LINKS</span></span>

[<span data-ttu-id="bdc01-139">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="bdc01-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="bdc01-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="bdc01-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="bdc01-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="bdc01-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

