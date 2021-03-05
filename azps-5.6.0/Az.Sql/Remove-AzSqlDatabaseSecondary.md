---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 566081ea78137c3816ecee58e76a4811c7f54f62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961368"
---
# <span data-ttu-id="c00aa-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c00aa-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="c00aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c00aa-102">SYNOPSIS</span></span>
<span data-ttu-id="c00aa-103">Прерывает репликацию данных между SQL и указанной вторичной базой данных.</span><span class="sxs-lookup"><span data-stu-id="c00aa-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="c00aa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c00aa-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c00aa-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c00aa-105">DESCRIPTION</span></span>
<span data-ttu-id="c00aa-106">Cmdlet **Remove-AzSqlDataBaseSecondary** устраняет прерывание связи гео-репликации.</span><span class="sxs-lookup"><span data-stu-id="c00aa-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="c00aa-107">Этот cmdlet заменяет Stop-AzSqlDatabaseCopy.</span><span class="sxs-lookup"><span data-stu-id="c00aa-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="c00aa-108">Синхронизация репликации не будет синхронизироваться до прекращения действия.</span><span class="sxs-lookup"><span data-stu-id="c00aa-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="c00aa-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c00aa-109">EXAMPLES</span></span>

## <span data-ttu-id="c00aa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c00aa-110">PARAMETERS</span></span>

### <span data-ttu-id="c00aa-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c00aa-111">-DatabaseName</span></span>
<span data-ttu-id="c00aa-112">Указывает имя основной базы данных Azure SQL, которая содержит связь репликации, удаляемую этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c00aa-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c00aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c00aa-113">-DefaultProfile</span></span>
<span data-ttu-id="c00aa-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c00aa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c00aa-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c00aa-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="c00aa-116">Имя группы ресурсов партнера.</span><span class="sxs-lookup"><span data-stu-id="c00aa-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="c00aa-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="c00aa-117">-PartnerServerName</span></span>
<span data-ttu-id="c00aa-118">Указывает имя партнера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c00aa-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="c00aa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c00aa-119">-ResourceGroupName</span></span>
<span data-ttu-id="c00aa-120">Указывает имя группы ресурсов, связанной со ссылкой на репликацию, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c00aa-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="c00aa-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c00aa-121">-ServerName</span></span>
<span data-ttu-id="c00aa-122">Указывает имя конечного SQL Server, для которого нужно удалить ссылку репликации.</span><span class="sxs-lookup"><span data-stu-id="c00aa-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="c00aa-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c00aa-123">-Confirm</span></span>
<span data-ttu-id="c00aa-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c00aa-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c00aa-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c00aa-125">-WhatIf</span></span>
<span data-ttu-id="c00aa-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c00aa-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c00aa-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c00aa-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c00aa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c00aa-128">CommonParameters</span></span>
<span data-ttu-id="c00aa-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c00aa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c00aa-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c00aa-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c00aa-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c00aa-131">INPUTS</span></span>

### <span data-ttu-id="c00aa-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c00aa-132">System.String</span></span>

## <span data-ttu-id="c00aa-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c00aa-133">OUTPUTS</span></span>

### <span data-ttu-id="c00aa-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="c00aa-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="c00aa-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c00aa-135">NOTES</span></span>

## <span data-ttu-id="c00aa-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c00aa-136">RELATED LINKS</span></span>

[<span data-ttu-id="c00aa-137">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c00aa-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="c00aa-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c00aa-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="c00aa-139">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="c00aa-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
