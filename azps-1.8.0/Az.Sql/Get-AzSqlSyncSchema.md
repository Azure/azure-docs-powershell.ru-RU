---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
ms.openlocfilehash: 7e6e060b2ad9e05a0a2789202e74f093f0366749
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728912"
---
# <span data-ttu-id="16c2a-101">Get-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="16c2a-101">Get-AzSqlSyncSchema</span></span>

## <span data-ttu-id="16c2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16c2a-102">SYNOPSIS</span></span>
<span data-ttu-id="16c2a-103">Возвращает сведения о схеме синхронизации базы данных участника или базы данных основного сервера.</span><span class="sxs-lookup"><span data-stu-id="16c2a-103">Returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="16c2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16c2a-104">SYNTAX</span></span>

```
Get-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16c2a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16c2a-105">DESCRIPTION</span></span>
<span data-ttu-id="16c2a-106">Командлет **Get-AzSqlSyncSchema** возвращает сведения о схеме синхронизации базы данных участника или базы данных основного сервера.</span><span class="sxs-lookup"><span data-stu-id="16c2a-106">The **Get-AzSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="16c2a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16c2a-107">EXAMPLES</span></span>

### <span data-ttu-id="16c2a-108">Пример 1,1: получение схемы синхронизации для базы данных-концентратора</span><span class="sxs-lookup"><span data-stu-id="16c2a-108">Example 1.1: Get the sync schema for a hub database</span></span>
```
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="16c2a-109">Эта команда получает схему синхронизации для базы данных Hub в группе "Синхронизация" syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="16c2a-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="16c2a-110">Пример 1,2: получение схемы синхронизации для базы данных HUB и развертывание таблиц</span><span class="sxs-lookup"><span data-stu-id="16c2a-110">Example 1.2: Get the sync schema for a hub database, and expand Tables</span></span>
```
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

<span data-ttu-id="16c2a-111">Эта команда получает схему синхронизации для базы данных Hub в свойстве "Синхронизация группы syncGroup01 и расширение таблиц".</span><span class="sxs-lookup"><span data-stu-id="16c2a-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="16c2a-112">Пример 2: получение схемы синхронизации для базы данных участника</span><span class="sxs-lookup"><span data-stu-id="16c2a-112">Example 2: Get the sync schema for a member database</span></span>
```
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="16c2a-113">Эта команда получает схему синхронизации для базы данных участников в syncMember01е синхронизации членов.</span><span class="sxs-lookup"><span data-stu-id="16c2a-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="16c2a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16c2a-114">PARAMETERS</span></span>

### <span data-ttu-id="16c2a-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="16c2a-115">-DatabaseName</span></span>
<span data-ttu-id="16c2a-116">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="16c2a-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="16c2a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c2a-117">-DefaultProfile</span></span>
<span data-ttu-id="16c2a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="16c2a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16c2a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16c2a-119">-ResourceGroupName</span></span>
<span data-ttu-id="16c2a-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16c2a-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="16c2a-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="16c2a-121">-ServerName</span></span>
<span data-ttu-id="16c2a-122">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="16c2a-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="16c2a-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="16c2a-123">-SyncGroupName</span></span>
<span data-ttu-id="16c2a-124">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="16c2a-124">The sync group name.</span></span>

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

### <span data-ttu-id="16c2a-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="16c2a-125">-SyncMemberName</span></span>
<span data-ttu-id="16c2a-126">Имя элемента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="16c2a-126">The sync member name.</span></span>

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

### <span data-ttu-id="16c2a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c2a-127">CommonParameters</span></span>
<span data-ttu-id="16c2a-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16c2a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c2a-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16c2a-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c2a-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16c2a-130">INPUTS</span></span>

### <span data-ttu-id="16c2a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="16c2a-131">System.String</span></span>

## <span data-ttu-id="16c2a-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16c2a-132">OUTPUTS</span></span>

### <span data-ttu-id="16c2a-133">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="16c2a-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

## <span data-ttu-id="16c2a-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="16c2a-134">NOTES</span></span>

## <span data-ttu-id="16c2a-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16c2a-135">RELATED LINKS</span></span>
