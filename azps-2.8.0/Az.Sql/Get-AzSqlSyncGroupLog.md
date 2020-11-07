---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: 0343cddd12fdf1fe438ec2c4c9c3c5763719cd43
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906618"
---
# <span data-ttu-id="9ea15-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="9ea15-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="9ea15-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ea15-102">SYNOPSIS</span></span>
<span data-ttu-id="9ea15-103">Возвращает журналы группы синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9ea15-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="9ea15-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ea15-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ea15-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ea15-105">DESCRIPTION</span></span>
<span data-ttu-id="9ea15-106">Командлет **Get-AzSqlSyncGroupLog** возвращает журналы группы синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9ea15-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="9ea15-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ea15-107">EXAMPLES</span></span>

### <span data-ttu-id="9ea15-108">Пример 1: получение журналов группы синхронизации Azure SQL</span><span class="sxs-lookup"><span data-stu-id="9ea15-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="9ea15-109">Эта команда получает журналы группы синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9ea15-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="9ea15-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ea15-110">PARAMETERS</span></span>

### <span data-ttu-id="9ea15-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9ea15-111">-DatabaseName</span></span>
<span data-ttu-id="9ea15-112">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9ea15-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="9ea15-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ea15-113">-DefaultProfile</span></span>
<span data-ttu-id="9ea15-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9ea15-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ea15-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="9ea15-115">-EndTime</span></span>
<span data-ttu-id="9ea15-116">Время завершения журналов для запроса.</span><span class="sxs-lookup"><span data-stu-id="9ea15-116">The end time of the logs to query.</span></span>

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

### <span data-ttu-id="9ea15-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="9ea15-117">-LogLevel</span></span>
<span data-ttu-id="9ea15-118">Тип журналов для запроса.</span><span class="sxs-lookup"><span data-stu-id="9ea15-118">The type of the logs to query.</span></span>
<span data-ttu-id="9ea15-119">Допустимые значения: "ошибка", "предупреждение", "успех" и "все".</span><span class="sxs-lookup"><span data-stu-id="9ea15-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

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

### <span data-ttu-id="9ea15-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ea15-120">-ResourceGroupName</span></span>
<span data-ttu-id="9ea15-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ea15-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="9ea15-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9ea15-122">-ServerName</span></span>
<span data-ttu-id="9ea15-123">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9ea15-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="9ea15-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9ea15-124">-StartTime</span></span>
<span data-ttu-id="9ea15-125">Время запуска журналов для запроса.</span><span class="sxs-lookup"><span data-stu-id="9ea15-125">The start time of the logs to query.</span></span>

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

### <span data-ttu-id="9ea15-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="9ea15-126">-SyncGroupName</span></span>
<span data-ttu-id="9ea15-127">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="9ea15-127">The sync group name.</span></span>

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

### <span data-ttu-id="9ea15-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ea15-128">CommonParameters</span></span>
<span data-ttu-id="9ea15-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ea15-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ea15-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ea15-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ea15-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ea15-131">INPUTS</span></span>

### <span data-ttu-id="9ea15-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9ea15-132">System.String</span></span>

## <span data-ttu-id="9ea15-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ea15-133">OUTPUTS</span></span>

### <span data-ttu-id="9ea15-134">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="9ea15-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="9ea15-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ea15-135">NOTES</span></span>

## <span data-ttu-id="9ea15-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ea15-136">RELATED LINKS</span></span>
