---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
ms.openlocfilehash: e32f693b5f0bfc114f3ac40a4fc5761ec3a3ca70
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999214"
---
# <span data-ttu-id="5fae5-101">Get-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="5fae5-101">Get-AzSqlSyncSchema</span></span>

## <span data-ttu-id="5fae5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fae5-102">SYNOPSIS</span></span>
<span data-ttu-id="5fae5-103">Возвращает сведения о схеме синхронизации базы данных или центральной базы данных.</span><span class="sxs-lookup"><span data-stu-id="5fae5-103">Returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="5fae5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5fae5-104">SYNTAX</span></span>

```
Get-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fae5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fae5-105">DESCRIPTION</span></span>
<span data-ttu-id="5fae5-106">Командалет **Get-AzSqlSyncSchema** возвращает сведения о схеме синхронизации базы данных участника или центральной базы данных.</span><span class="sxs-lookup"><span data-stu-id="5fae5-106">The **Get-AzSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="5fae5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5fae5-107">EXAMPLES</span></span>

### <span data-ttu-id="5fae5-108">Пример 1. Получить схему синхронизации для базы данных концентратора</span><span class="sxs-lookup"><span data-stu-id="5fae5-108">Example 1: Get the sync schema for a hub database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="5fae5-109">Эта команда получает схему синхронизации центральной базы данных в группе синхронизацииGroup01.</span><span class="sxs-lookup"><span data-stu-id="5fae5-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="5fae5-110">Пример 2. Получить схему синхронизации для базы данных концентратора и развернуть таблицы</span><span class="sxs-lookup"><span data-stu-id="5fae5-110">Example 2: Get the sync schema for a hub database, and expand Tables</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
Columns    : {column1, column2}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_1
QuotedName : [dbo].[Table_1]

Columns    : {column2, column4}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_2
QuotedName : [dbo].[Table_2]
```

<span data-ttu-id="5fae5-111">Эта команда получает схему синхронизации для базы данных концентратора в группе синхронизацииGroup01 и расширяет свойство "Таблицы".</span><span class="sxs-lookup"><span data-stu-id="5fae5-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="5fae5-112">Пример 3. Получить схему синхронизации для базы данных участника</span><span class="sxs-lookup"><span data-stu-id="5fae5-112">Example 3: Get the sync schema for a member database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="5fae5-113">Эта команда получает схему синхронизации для базы данных ее членов в syncMember01.</span><span class="sxs-lookup"><span data-stu-id="5fae5-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="5fae5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fae5-114">PARAMETERS</span></span>

### <span data-ttu-id="5fae5-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5fae5-115">-DatabaseName</span></span>
<span data-ttu-id="5fae5-116">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="5fae5-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="5fae5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fae5-117">-DefaultProfile</span></span>
<span data-ttu-id="5fae5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5fae5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5fae5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fae5-119">-ResourceGroupName</span></span>
<span data-ttu-id="5fae5-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5fae5-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="5fae5-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5fae5-121">-ServerName</span></span>
<span data-ttu-id="5fae5-122">Имя службы Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5fae5-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="5fae5-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="5fae5-123">-SyncGroupName</span></span>
<span data-ttu-id="5fae5-124">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="5fae5-124">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fae5-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="5fae5-125">-SyncMemberName</span></span>
<span data-ttu-id="5fae5-126">Имя участника синхронизации.</span><span class="sxs-lookup"><span data-stu-id="5fae5-126">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fae5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fae5-127">CommonParameters</span></span>
<span data-ttu-id="5fae5-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fae5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fae5-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fae5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fae5-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5fae5-130">INPUTS</span></span>

### <span data-ttu-id="5fae5-131">System.String</span><span class="sxs-lookup"><span data-stu-id="5fae5-131">System.String</span></span>

## <span data-ttu-id="5fae5-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5fae5-132">OUTPUTS</span></span>

### <span data-ttu-id="5fae5-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="5fae5-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

## <span data-ttu-id="5fae5-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5fae5-134">NOTES</span></span>

## <span data-ttu-id="5fae5-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5fae5-135">RELATED LINKS</span></span>
