---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: f8e73860d87d9389f2099a29039d90e0ac0534d6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243227"
---
# <span data-ttu-id="d8f26-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="d8f26-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="d8f26-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8f26-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f26-103">Возвращает журналы группы синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d8f26-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="d8f26-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8f26-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8f26-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8f26-105">DESCRIPTION</span></span>
<span data-ttu-id="d8f26-106">Командлет **Get-AzSqlSyncGroupLog** возвращает журналы группы синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d8f26-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="d8f26-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8f26-107">EXAMPLES</span></span>

### <span data-ttu-id="d8f26-108">Пример 1: получение журналов группы синхронизации Azure SQL</span><span class="sxs-lookup"><span data-stu-id="d8f26-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="d8f26-109">Эта команда получает журналы группы синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d8f26-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="d8f26-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8f26-110">PARAMETERS</span></span>

### <span data-ttu-id="d8f26-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d8f26-111">-DatabaseName</span></span>
<span data-ttu-id="d8f26-112">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d8f26-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d8f26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f26-113">-DefaultProfile</span></span>
<span data-ttu-id="d8f26-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d8f26-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8f26-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="d8f26-115">-EndTime</span></span>
<span data-ttu-id="d8f26-116">Время завершения журналов для запроса.</span><span class="sxs-lookup"><span data-stu-id="d8f26-116">The end time of the logs to query.</span></span>

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

### <span data-ttu-id="d8f26-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="d8f26-117">-LogLevel</span></span>
<span data-ttu-id="d8f26-118">Тип журналов для запроса.</span><span class="sxs-lookup"><span data-stu-id="d8f26-118">The type of the logs to query.</span></span>
<span data-ttu-id="d8f26-119">Допустимые значения: "ошибка", "предупреждение", "успех" и "все".</span><span class="sxs-lookup"><span data-stu-id="d8f26-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

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

### <span data-ttu-id="d8f26-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f26-120">-ResourceGroupName</span></span>
<span data-ttu-id="d8f26-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d8f26-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="d8f26-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d8f26-122">-ServerName</span></span>
<span data-ttu-id="d8f26-123">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d8f26-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d8f26-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d8f26-124">-StartTime</span></span>
<span data-ttu-id="d8f26-125">Время запуска журналов для запроса.</span><span class="sxs-lookup"><span data-stu-id="d8f26-125">The start time of the logs to query.</span></span>

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

### <span data-ttu-id="d8f26-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f26-126">-SyncGroupName</span></span>
<span data-ttu-id="d8f26-127">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="d8f26-127">The sync group name.</span></span>

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

### <span data-ttu-id="d8f26-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f26-128">CommonParameters</span></span>
<span data-ttu-id="d8f26-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8f26-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f26-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8f26-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f26-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8f26-131">INPUTS</span></span>

### <span data-ttu-id="d8f26-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d8f26-132">System.String</span></span>

## <span data-ttu-id="d8f26-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8f26-133">OUTPUTS</span></span>

### <span data-ttu-id="d8f26-134">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="d8f26-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="d8f26-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8f26-135">NOTES</span></span>

## <span data-ttu-id="d8f26-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8f26-136">RELATED LINKS</span></span>