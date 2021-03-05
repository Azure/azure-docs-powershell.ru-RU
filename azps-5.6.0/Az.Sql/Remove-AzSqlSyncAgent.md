---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: 30c0cca7fb1d8eab2c5d0abe4d6c0d556cc92d7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995140"
---
# <span data-ttu-id="7a0e7-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7a0e7-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="7a0e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a0e7-102">SYNOPSIS</span></span>
<span data-ttu-id="7a0e7-103">Удаляет агент синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7a0e7-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="7a0e7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7a0e7-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a0e7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a0e7-105">DESCRIPTION</span></span>
<span data-ttu-id="7a0e7-106">При **этом удаляется** агент синхронизации Azure SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="7a0e7-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="7a0e7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7a0e7-107">EXAMPLES</span></span>

### <span data-ttu-id="7a0e7-108">Пример 1. Удаление агента синхронизации</span><span class="sxs-lookup"><span data-stu-id="7a0e7-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="7a0e7-109">Эта команда удаляет агент синхронизации Azure SQL syncAgent01.</span><span class="sxs-lookup"><span data-stu-id="7a0e7-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="7a0e7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a0e7-110">PARAMETERS</span></span>

### <span data-ttu-id="7a0e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a0e7-111">-DefaultProfile</span></span>
<span data-ttu-id="7a0e7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7a0e7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a0e7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7a0e7-113">-Force</span></span>
<span data-ttu-id="7a0e7-114">Пропустить сообщение подтверждения для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="7a0e7-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="7a0e7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7a0e7-115">-Name</span></span>
<span data-ttu-id="7a0e7-116">Имя агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="7a0e7-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a0e7-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a0e7-117">-PassThru</span></span>
<span data-ttu-id="7a0e7-118">Определяет, возвращает ли удален агент синхронизации</span><span class="sxs-lookup"><span data-stu-id="7a0e7-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="7a0e7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a0e7-119">-ResourceGroupName</span></span>
<span data-ttu-id="7a0e7-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7a0e7-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="7a0e7-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7a0e7-121">-ServerName</span></span>
<span data-ttu-id="7a0e7-122">Имя Azure, SQL Server агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="7a0e7-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="7a0e7-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a0e7-123">-Confirm</span></span>
<span data-ttu-id="7a0e7-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a0e7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a0e7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a0e7-125">-WhatIf</span></span>
<span data-ttu-id="7a0e7-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a0e7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a0e7-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7a0e7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a0e7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a0e7-128">CommonParameters</span></span>
<span data-ttu-id="7a0e7-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a0e7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a0e7-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a0e7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a0e7-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a0e7-131">INPUTS</span></span>

### <span data-ttu-id="7a0e7-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7a0e7-132">System.String</span></span>

## <span data-ttu-id="7a0e7-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7a0e7-133">OUTPUTS</span></span>

### <span data-ttu-id="7a0e7-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="7a0e7-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="7a0e7-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7a0e7-135">NOTES</span></span>

## <span data-ttu-id="7a0e7-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a0e7-136">RELATED LINKS</span></span>

[<span data-ttu-id="7a0e7-137">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7a0e7-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="7a0e7-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7a0e7-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

