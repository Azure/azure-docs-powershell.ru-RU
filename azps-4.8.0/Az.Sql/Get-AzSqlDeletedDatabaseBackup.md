---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
ms.openlocfilehash: d534ddc9c076d0e7c2ea611d6fdb15ae22e84846
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078686"
---
# <span data-ttu-id="46f3c-101">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="46f3c-101">Get-AzSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="46f3c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="46f3c-103">Получает удаленную базу данных, которую можно восстановить.</span><span class="sxs-lookup"><span data-stu-id="46f3c-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="46f3c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46f3c-104">SYNTAX</span></span>

```
Get-AzSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>] [[-DeletionDate] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46f3c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46f3c-105">DESCRIPTION</span></span>
<span data-ttu-id="46f3c-106">Командлет **Get-AzSqlDeletedDatabaseBackup** возвращает указанное удаленное резервное копирование базы данных SQL, которое можно восстановить, или все удаленные резервные копии, которые можно восстановить.</span><span class="sxs-lookup"><span data-stu-id="46f3c-106">The **Get-AzSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="46f3c-107">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="46f3c-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="46f3c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46f3c-108">EXAMPLES</span></span>

### <span data-ttu-id="46f3c-109">Пример 1: получение всех удаленных резервных копий базы данных на сервере</span><span class="sxs-lookup"><span data-stu-id="46f3c-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="46f3c-110">Эта команда возвращает все удаленные резервные копии базы данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="46f3c-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="46f3c-111">Пример 2: получение указанной удаленной резервной копии базы данных</span><span class="sxs-lookup"><span data-stu-id="46f3c-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="46f3c-112">Эта команда возвращает удаленное резервное копирование базы данных для ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="46f3c-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="46f3c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46f3c-113">PARAMETERS</span></span>

### <span data-ttu-id="46f3c-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="46f3c-114">-DatabaseName</span></span>
<span data-ttu-id="46f3c-115">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="46f3c-115">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f3c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f3c-116">-DefaultProfile</span></span>
<span data-ttu-id="46f3c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="46f3c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46f3c-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="46f3c-118">-DeletionDate</span></span>
<span data-ttu-id="46f3c-119">Указывает дату удаления базы данных в виде объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="46f3c-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="46f3c-120">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="46f3c-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f3c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46f3c-121">-ResourceGroupName</span></span>
<span data-ttu-id="46f3c-122">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="46f3c-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="46f3c-123">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="46f3c-123">-ServerName</span></span>
<span data-ttu-id="46f3c-124">Указывает имя сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="46f3c-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="46f3c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46f3c-125">-Confirm</span></span>
<span data-ttu-id="46f3c-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="46f3c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46f3c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46f3c-127">-WhatIf</span></span>
<span data-ttu-id="46f3c-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="46f3c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46f3c-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="46f3c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46f3c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f3c-130">CommonParameters</span></span>
<span data-ttu-id="46f3c-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46f3c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f3c-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46f3c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f3c-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46f3c-133">INPUTS</span></span>

### <span data-ttu-id="46f3c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="46f3c-134">System.String</span></span>

### <span data-ttu-id="46f3c-135">System. Nullable "1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="46f3c-135">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="46f3c-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46f3c-136">OUTPUTS</span></span>

### <span data-ttu-id="46f3c-137">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDeletedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="46f3c-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="46f3c-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="46f3c-138">NOTES</span></span>

## <span data-ttu-id="46f3c-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46f3c-139">RELATED LINKS</span></span>

[<span data-ttu-id="46f3c-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46f3c-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="46f3c-141">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="46f3c-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
