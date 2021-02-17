---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: f8e73860d87d9389f2099a29039d90e0ac0534d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212500"
---
# <span data-ttu-id="b9a58-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="b9a58-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="b9a58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9a58-102">SYNOPSIS</span></span>
<span data-ttu-id="b9a58-103">Возвращает журналы группы синхронизации баз SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b9a58-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="b9a58-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b9a58-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9a58-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9a58-105">DESCRIPTION</span></span>
<span data-ttu-id="b9a58-106">Чтобы получить журналы группы синхронизации базы данных Azure SQL Azure, возвращается cmdlet **Get-AzSqlSyncGroupLog.**</span><span class="sxs-lookup"><span data-stu-id="b9a58-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="b9a58-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b9a58-107">EXAMPLES</span></span>

### <span data-ttu-id="b9a58-108">Пример 1. Просмотр журналов группы синхронизации Azure SQL</span><span class="sxs-lookup"><span data-stu-id="b9a58-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="b9a58-109">Эта команда получает журналы группы синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b9a58-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="b9a58-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9a58-110">PARAMETERS</span></span>

### <span data-ttu-id="b9a58-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b9a58-111">-DatabaseName</span></span>
<span data-ttu-id="b9a58-112">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b9a58-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="b9a58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9a58-113">-DefaultProfile</span></span>
<span data-ttu-id="b9a58-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b9a58-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9a58-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b9a58-115">-EndTime</span></span>
<span data-ttu-id="b9a58-116">Время окончания запросов журналов.</span><span class="sxs-lookup"><span data-stu-id="b9a58-116">The end time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a58-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="b9a58-117">-LogLevel</span></span>
<span data-ttu-id="b9a58-118">Тип журналов для запроса.</span><span class="sxs-lookup"><span data-stu-id="b9a58-118">The type of the logs to query.</span></span>
<span data-ttu-id="b9a58-119">Допустимые значения: "Ошибка", "Предупреждение", "Успех" и "Все".</span><span class="sxs-lookup"><span data-stu-id="b9a58-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Error, Warning, Success, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a58-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9a58-120">-ResourceGroupName</span></span>
<span data-ttu-id="b9a58-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b9a58-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="b9a58-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b9a58-122">-ServerName</span></span>
<span data-ttu-id="b9a58-123">Имя службы Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b9a58-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="b9a58-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b9a58-124">-StartTime</span></span>
<span data-ttu-id="b9a58-125">Время начала запросов журналов.</span><span class="sxs-lookup"><span data-stu-id="b9a58-125">The start time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a58-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="b9a58-126">-SyncGroupName</span></span>
<span data-ttu-id="b9a58-127">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="b9a58-127">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9a58-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9a58-128">CommonParameters</span></span>
<span data-ttu-id="b9a58-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9a58-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9a58-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9a58-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9a58-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9a58-131">INPUTS</span></span>

### <span data-ttu-id="b9a58-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b9a58-132">System.String</span></span>

## <span data-ttu-id="b9a58-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b9a58-133">OUTPUTS</span></span>

### <span data-ttu-id="b9a58-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="b9a58-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="b9a58-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b9a58-135">NOTES</span></span>

## <span data-ttu-id="b9a58-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9a58-136">RELATED LINKS</span></span>
