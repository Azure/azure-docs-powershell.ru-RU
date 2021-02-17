---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 4353a61efd0141947879ad6795c321f5ed43e1d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230097"
---
# <span data-ttu-id="f3805-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f3805-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="f3805-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3805-102">SYNOPSIS</span></span>
<span data-ttu-id="f3805-103">Прерывает репликацию данных между SQL и указанной вторичной базой данных.</span><span class="sxs-lookup"><span data-stu-id="f3805-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="f3805-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f3805-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3805-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3805-105">DESCRIPTION</span></span>
<span data-ttu-id="f3805-106">Cmdlet **Remove-AzSqlDataBaseSecondary** устраняет прерывание связи гео-репликации.</span><span class="sxs-lookup"><span data-stu-id="f3805-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="f3805-107">Этот cmdlet заменяет Stop-AzSqlDatabaseCopy.</span><span class="sxs-lookup"><span data-stu-id="f3805-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="f3805-108">До прекращения действия синхронизации репликации не будет.</span><span class="sxs-lookup"><span data-stu-id="f3805-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="f3805-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f3805-109">EXAMPLES</span></span>

## <span data-ttu-id="f3805-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3805-110">PARAMETERS</span></span>

### <span data-ttu-id="f3805-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f3805-111">-DatabaseName</span></span>
<span data-ttu-id="f3805-112">Указывает имя основной базы данных Azure SQL, которая содержит ссылку репликации, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3805-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f3805-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3805-113">-DefaultProfile</span></span>
<span data-ttu-id="f3805-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f3805-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3805-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3805-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="f3805-116">Имя группы ресурсов партнера.</span><span class="sxs-lookup"><span data-stu-id="f3805-116">Specifies the name of the partner  resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3805-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="f3805-117">-PartnerServerName</span></span>
<span data-ttu-id="f3805-118">Указывает имя партнера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f3805-118">Specifies the name of the partner SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3805-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3805-119">-ResourceGroupName</span></span>
<span data-ttu-id="f3805-120">Указывает имя группы ресурсов, связанной со ссылкой на репликацию, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f3805-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="f3805-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f3805-121">-ServerName</span></span>
<span data-ttu-id="f3805-122">Указывает имя конечного SQL Server, для которого нужно удалить ссылку репликации.</span><span class="sxs-lookup"><span data-stu-id="f3805-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="f3805-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3805-123">-Confirm</span></span>
<span data-ttu-id="f3805-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3805-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3805-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3805-125">-WhatIf</span></span>
<span data-ttu-id="f3805-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3805-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3805-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f3805-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3805-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3805-128">CommonParameters</span></span>
<span data-ttu-id="f3805-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3805-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3805-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3805-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3805-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3805-131">INPUTS</span></span>

### <span data-ttu-id="f3805-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f3805-132">System.String</span></span>

## <span data-ttu-id="f3805-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f3805-133">OUTPUTS</span></span>

### <span data-ttu-id="f3805-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="f3805-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="f3805-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f3805-135">NOTES</span></span>

## <span data-ttu-id="f3805-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3805-136">RELATED LINKS</span></span>

[<span data-ttu-id="f3805-137">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f3805-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="f3805-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f3805-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="f3805-139">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="f3805-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
