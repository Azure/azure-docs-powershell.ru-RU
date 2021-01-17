---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: f8e73860d87d9389f2099a29039d90e0ac0534d6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413260"
---
# <span data-ttu-id="9724b-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="9724b-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="9724b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9724b-102">SYNOPSIS</span></span>
<span data-ttu-id="9724b-103">Возвращает журналы группы синхронизации баз SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9724b-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="9724b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9724b-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9724b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9724b-105">DESCRIPTION</span></span>
<span data-ttu-id="9724b-106">Чтобы получить журналы группы синхронизации базы данных Azure SQL Azure, возвращается cmdlet **Get-AzSqlSyncGroupLog.**</span><span class="sxs-lookup"><span data-stu-id="9724b-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="9724b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9724b-107">EXAMPLES</span></span>

### <span data-ttu-id="9724b-108">Пример 1. Просмотр журналов группы синхронизации Azure SQL</span><span class="sxs-lookup"><span data-stu-id="9724b-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="9724b-109">Эта команда получает журналы группы синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9724b-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="9724b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9724b-110">PARAMETERS</span></span>

### <span data-ttu-id="9724b-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9724b-111">-DatabaseName</span></span>
<span data-ttu-id="9724b-112">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9724b-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="9724b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9724b-113">-DefaultProfile</span></span>
<span data-ttu-id="9724b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9724b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9724b-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="9724b-115">-EndTime</span></span>
<span data-ttu-id="9724b-116">Время окончания запросов журналов.</span><span class="sxs-lookup"><span data-stu-id="9724b-116">The end time of the logs to query.</span></span>

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

### <span data-ttu-id="9724b-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="9724b-117">-LogLevel</span></span>
<span data-ttu-id="9724b-118">Тип журналов для запроса.</span><span class="sxs-lookup"><span data-stu-id="9724b-118">The type of the logs to query.</span></span>
<span data-ttu-id="9724b-119">Допустимые значения: "Ошибка", "Предупреждение", "Успех" и "Все".</span><span class="sxs-lookup"><span data-stu-id="9724b-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

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

### <span data-ttu-id="9724b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9724b-120">-ResourceGroupName</span></span>
<span data-ttu-id="9724b-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9724b-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="9724b-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9724b-122">-ServerName</span></span>
<span data-ttu-id="9724b-123">Имя службы Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9724b-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="9724b-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9724b-124">-StartTime</span></span>
<span data-ttu-id="9724b-125">Время начала запросов журналов.</span><span class="sxs-lookup"><span data-stu-id="9724b-125">The start time of the logs to query.</span></span>

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

### <span data-ttu-id="9724b-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="9724b-126">-SyncGroupName</span></span>
<span data-ttu-id="9724b-127">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="9724b-127">The sync group name.</span></span>

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

### <span data-ttu-id="9724b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9724b-128">CommonParameters</span></span>
<span data-ttu-id="9724b-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9724b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9724b-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9724b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9724b-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9724b-131">INPUTS</span></span>

### <span data-ttu-id="9724b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9724b-132">System.String</span></span>

## <span data-ttu-id="9724b-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9724b-133">OUTPUTS</span></span>

### <span data-ttu-id="9724b-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="9724b-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="9724b-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9724b-135">NOTES</span></span>

## <span data-ttu-id="9724b-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9724b-136">RELATED LINKS</span></span>
