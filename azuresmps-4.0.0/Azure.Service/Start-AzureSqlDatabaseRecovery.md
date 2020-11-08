---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075423"
---
# <span data-ttu-id="bc42c-101">Start-AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="bc42c-101">Start-AzureSqlDatabaseRecovery</span></span>

## <span data-ttu-id="bc42c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc42c-102">SYNOPSIS</span></span>
<span data-ttu-id="bc42c-103">Инициирует запрос на восстановление для базы данных.</span><span class="sxs-lookup"><span data-stu-id="bc42c-103">Initiates a restore request for a database.</span></span>

## <span data-ttu-id="bc42c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc42c-104">SYNTAX</span></span>

### <span data-ttu-id="bc42c-105">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="bc42c-105">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bc42c-106">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="bc42c-106">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bc42c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc42c-107">DESCRIPTION</span></span>
<span data-ttu-id="bc42c-108">Командлет **Start-AzureSqlDatabaseRecovery** инициирует запрос на восстановление для реальной или удаленной базы данных.</span><span class="sxs-lookup"><span data-stu-id="bc42c-108">The **Start-AzureSqlDatabaseRecovery** cmdlet initiates a restore request for a live or dropped database.</span></span>
<span data-ttu-id="bc42c-109">Этот командлет поддерживает базовое восстановление, которое использует последнюю известную доступную резервную копию для базы данных.</span><span class="sxs-lookup"><span data-stu-id="bc42c-109">This cmdlet supports basic recovery that uses the last known available backup for the database.</span></span>
<span data-ttu-id="bc42c-110">Операция восстановления создает новую базу данных.</span><span class="sxs-lookup"><span data-stu-id="bc42c-110">The recovery operation creates a new database.</span></span>
<span data-ttu-id="bc42c-111">Если вы восстановите базу данных Live на том же сервере, необходимо указать другое имя для новой базы данных.</span><span class="sxs-lookup"><span data-stu-id="bc42c-111">If you recover a live database on the same server, you must specify a different name for the new database.</span></span>

<span data-ttu-id="bc42c-112">Чтобы выполнить восстановление базы данных на момент времени, вместо этого используйте командлет **Start-AzureSqlDatabaseRestore** .</span><span class="sxs-lookup"><span data-stu-id="bc42c-112">To do a point in time restore for a database, use the **Start-AzureSqlDatabaseRestore** cmdlet instead.</span></span>

## <span data-ttu-id="bc42c-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc42c-113">EXAMPLES</span></span>

### <span data-ttu-id="bc42c-114">Пример 1: восстановление базы данных, указанной как объект</span><span class="sxs-lookup"><span data-stu-id="bc42c-114">Example 1: Recover a database specified as an object</span></span>
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="bc42c-115">Первая команда получает объект базы данных с помощью командлета **Get-AzureSqlRecoverableDatabase** .</span><span class="sxs-lookup"><span data-stu-id="bc42c-115">The first command gets a database object by using the **Get-AzureSqlRecoverableDatabase** cmdlet.</span></span>
<span data-ttu-id="bc42c-116">Команда сохраняет этот объект в переменной $Database.</span><span class="sxs-lookup"><span data-stu-id="bc42c-116">The command stores that object in the $Database variable.</span></span>

<span data-ttu-id="bc42c-117">Во второй команде база данных, сохраненная в $Database, будет восстановлена.</span><span class="sxs-lookup"><span data-stu-id="bc42c-117">The second command recovers the database stored in $Database.</span></span>

### <span data-ttu-id="bc42c-118">Пример 2: восстановление базы данных с указанным именем</span><span class="sxs-lookup"><span data-stu-id="bc42c-118">Example 2: Recover a database specified by name</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="bc42c-119">Эта команда используется для восстановления базы данных с использованием имени базы данных.</span><span class="sxs-lookup"><span data-stu-id="bc42c-119">This command recovers a database using the database name.</span></span>

## <span data-ttu-id="bc42c-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc42c-120">PARAMETERS</span></span>

### <span data-ttu-id="bc42c-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="bc42c-121">-Profile</span></span>
<span data-ttu-id="bc42c-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bc42c-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bc42c-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bc42c-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc42c-124">-SourceDatabase</span><span class="sxs-lookup"><span data-stu-id="bc42c-124">-SourceDatabase</span></span>
<span data-ttu-id="bc42c-125">Указывает объект базы данных, представляющий базу данных, которую этот командлет подявляет.</span><span class="sxs-lookup"><span data-stu-id="bc42c-125">Specifies the database object that represents the database that this cmdlet recovers.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc42c-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="bc42c-126">-SourceDatabaseName</span></span>
<span data-ttu-id="bc42c-127">Указывает имя базы данных, которую этот командлет обнаружить.</span><span class="sxs-lookup"><span data-stu-id="bc42c-127">Specifies the name of the database that this cmdlet recovers.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc42c-128">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="bc42c-128">-SourceServerName</span></span>
<span data-ttu-id="bc42c-129">Указывает имя сервера, на котором находится база данных источника и что она запущена, или на которой была выполнена удаленная база данных.</span><span class="sxs-lookup"><span data-stu-id="bc42c-129">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc42c-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="bc42c-130">-TargetDatabaseName</span></span>
<span data-ttu-id="bc42c-131">Указывает имя восстановленной базы данных.</span><span class="sxs-lookup"><span data-stu-id="bc42c-131">Specifies the name of the recovered database.</span></span>
<span data-ttu-id="bc42c-132">Если исходная база данных по-прежнему находится в режиме реального времени, для восстановления ее на том же сервере необходимо указать имя, отличное от имени базы данных-источника.</span><span class="sxs-lookup"><span data-stu-id="bc42c-132">If the source database is still live, in order to recover it to the same server, you must specify a name that differs from the source database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc42c-133">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="bc42c-133">-TargetServerName</span></span>
<span data-ttu-id="bc42c-134">Указывает имя сервера, на который нужно восстановить базу данных.</span><span class="sxs-lookup"><span data-stu-id="bc42c-134">Specifies the name of the server to which to restore a database.</span></span>
<span data-ttu-id="bc42c-135">Базу данных можно восстановить на том же или другом сервере.</span><span class="sxs-lookup"><span data-stu-id="bc42c-135">You can restore a database to the same server or to a different server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc42c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc42c-136">CommonParameters</span></span>
<span data-ttu-id="bc42c-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc42c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc42c-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc42c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc42c-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc42c-139">INPUTS</span></span>

### <span data-ttu-id="bc42c-140">Microsoft. WindowsAzure. Management. SQL. Models. RecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="bc42c-140">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="bc42c-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc42c-141">OUTPUTS</span></span>

### <span data-ttu-id="bc42c-142">Microsoft. WindowsAzure. Management. SQL. Models. RecoverDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="bc42c-142">Microsoft.WindowsAzure.Management.Sql.Models.RecoverDatabaseOperation</span></span>

## <span data-ttu-id="bc42c-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc42c-143">NOTES</span></span>
* <span data-ttu-id="bc42c-144">Для запуска этого командлета необходимо использовать проверку подлинности на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="bc42c-144">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="bc42c-145">На компьютере, на котором вы запускаете этот командлет, выполните следующие команды:</span><span class="sxs-lookup"><span data-stu-id="bc42c-145">Run the following commands on the computer where you run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="bc42c-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc42c-146">RELATED LINKS</span></span>

[<span data-ttu-id="bc42c-147">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="bc42c-147">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="bc42c-148">Создание запроса на восстановление базы данных</span><span class="sxs-lookup"><span data-stu-id="bc42c-148">Create Database Recovery Request</span></span>](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[<span data-ttu-id="bc42c-149">Георепликация в базе данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="bc42c-149">Geo-Replication in Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[<span data-ttu-id="bc42c-150">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="bc42c-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="bc42c-151">Get-AzureSqlRecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="bc42c-151">Get-AzureSqlRecoverableDatabase</span></span>](./Get-AzureSqlRecoverableDatabase.md)

[<span data-ttu-id="bc42c-152">Start-AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="bc42c-152">Start-AzureSqlDatabaseRestore</span></span>](./Start-AzureSqlDatabaseRestore.md)


