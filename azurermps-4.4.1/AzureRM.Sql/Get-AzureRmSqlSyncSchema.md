---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
ms.openlocfilehash: ef66de2b12cf0ea723540c392a296d2d1c482505
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559455"
---
# <span data-ttu-id="12e95-101">Get-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="12e95-101">Get-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="12e95-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12e95-102">SYNOPSIS</span></span>
<span data-ttu-id="12e95-103">Возвращает сведения о схеме синхронизации базы данных участника или базы данных основного сервера.</span><span class="sxs-lookup"><span data-stu-id="12e95-103">Returns information about the sync schema of a member database or a hub database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12e95-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12e95-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12e95-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12e95-105">DESCRIPTION</span></span>
<span data-ttu-id="12e95-106">Командлет **Get-AzureRmSqlSyncSchema** возвращает сведения о схеме синхронизации базы данных участника или базы данных основного сервера.</span><span class="sxs-lookup"><span data-stu-id="12e95-106">The **Get-AzureRmSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="12e95-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12e95-107">EXAMPLES</span></span>

### <span data-ttu-id="12e95-108">Пример 1,1: получение схемы синхронизации для базы данных-концентратора</span><span class="sxs-lookup"><span data-stu-id="12e95-108">Example 1.1: Get the sync schema for a hub database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="12e95-109">Эта команда получает схему синхронизации для базы данных Hub в группе "Синхронизация" syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="12e95-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="12e95-110">Пример 1,2: получение схемы синхронизации для базы данных HUB и развертывание таблиц</span><span class="sxs-lookup"><span data-stu-id="12e95-110">Example 1.2: Get the sync schema for a hub database, and expand Tables</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
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

<span data-ttu-id="12e95-111">Эта команда получает схему синхронизации для базы данных Hub в свойстве "Синхронизация группы syncGroup01 и расширение таблиц".</span><span class="sxs-lookup"><span data-stu-id="12e95-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="12e95-112">Пример 2: получение схемы синхронизации для базы данных участника</span><span class="sxs-lookup"><span data-stu-id="12e95-112">Example 2: Get the sync schema for a member database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="12e95-113">Эта команда получает схему синхронизации для базы данных участников в syncMember01е синхронизации членов.</span><span class="sxs-lookup"><span data-stu-id="12e95-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="12e95-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12e95-114">PARAMETERS</span></span>

### <span data-ttu-id="12e95-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="12e95-115">-DatabaseName</span></span>
<span data-ttu-id="12e95-116">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="12e95-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="12e95-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e95-117">-ResourceGroupName</span></span>
<span data-ttu-id="12e95-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12e95-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="12e95-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="12e95-119">-ServerName</span></span>
<span data-ttu-id="12e95-120">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="12e95-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="12e95-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="12e95-121">-SyncGroupName</span></span>
<span data-ttu-id="12e95-122">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="12e95-122">The sync group name.</span></span>

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

### <span data-ttu-id="12e95-123">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="12e95-123">-SyncMemberName</span></span>
<span data-ttu-id="12e95-124">Имя элемента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="12e95-124">The sync member name.</span></span>

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

### <span data-ttu-id="12e95-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e95-125">-DefaultProfile</span></span>
<span data-ttu-id="12e95-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12e95-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e95-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e95-127">CommonParameters</span></span>
<span data-ttu-id="12e95-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12e95-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e95-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12e95-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e95-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12e95-130">INPUTS</span></span>

## <span data-ttu-id="12e95-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12e95-131">OUTPUTS</span></span>

### <span data-ttu-id="12e95-132">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="12e95-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

### <span data-ttu-id="12e95-133">Таблицы: Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncFullSchemaTableModel</span><span class="sxs-lookup"><span data-stu-id="12e95-133">Tables: Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaTableModel</span></span>

### <span data-ttu-id="12e95-134">Столбцы: Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncFullSchemaColumnModel</span><span class="sxs-lookup"><span data-stu-id="12e95-134">Columns: Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaColumnModel</span></span>

## <span data-ttu-id="12e95-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="12e95-135">NOTES</span></span>

## <span data-ttu-id="12e95-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12e95-136">RELATED LINKS</span></span>

