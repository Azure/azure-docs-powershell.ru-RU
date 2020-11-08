---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 3005E411-9466-4602-8E07-F4EF8804AB2A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22bff485bf49e0ec5f482e1325af661862583605
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075752"
---
# <span data-ttu-id="da48f-101">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="da48f-101">Start-AzureSqlDatabaseExport</span></span>

## <span data-ttu-id="da48f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da48f-102">SYNOPSIS</span></span>
<span data-ttu-id="da48f-103">Запускает операцию экспорта из базы данных SQL Azure в хранилище BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="da48f-103">Starts an export operation from an Azure SQL Database to Blob storage.</span></span>

## <span data-ttu-id="da48f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da48f-104">SYNTAX</span></span>

### <span data-ttu-id="da48f-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="da48f-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="da48f-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="da48f-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="da48f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da48f-107">DESCRIPTION</span></span>
<span data-ttu-id="da48f-108">Командлет **Start-AzureSqlDatabaseExport** запускает операцию экспорта из базы данных SQL Azure в хранилище BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="da48f-108">The **Start-AzureSqlDatabaseExport** cmdlet starts an export operation from an Azure SQL Database to Blob storage.</span></span>
<span data-ttu-id="da48f-109">Для операции требуется контекст подключения к серверу базы данных.</span><span class="sxs-lookup"><span data-stu-id="da48f-109">The operation requires a database server connection context.</span></span>
<span data-ttu-id="da48f-110">Используйте командлет Get-AzureSqlDatabaseImportExportStatus, чтобы получить состояние операции экспорта.</span><span class="sxs-lookup"><span data-stu-id="da48f-110">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the export operation.</span></span>

## <span data-ttu-id="da48f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da48f-111">EXAMPLES</span></span>

### <span data-ttu-id="da48f-112">Пример 1: экспорт базы данных</span><span class="sxs-lookup"><span data-stu-id="da48f-112">Example 1: Export a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credential $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $exportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="da48f-113">В этом примере инициируется процесс экспорта из базы данных Azure SQL с именем, хранящимся в переменной $DatabaseName, в хранилище BLOB-объектов, которое хранится в переменной $BlobName.</span><span class="sxs-lookup"><span data-stu-id="da48f-113">This example initiates an export process from the Azure SQL Database that has the name stored in the $DatabaseName variable to the Blob storage stored in the $BlobName variable.</span></span>

## <span data-ttu-id="da48f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da48f-114">PARAMETERS</span></span>

### <span data-ttu-id="da48f-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="da48f-115">-BlobName</span></span>
<span data-ttu-id="da48f-116">Указывает имя хранилища BLOB-объектов Azure, в которое этот командлет экспортирует базу данных.</span><span class="sxs-lookup"><span data-stu-id="da48f-116">Specifies the name of the Azure Blob storage into which this cmdlet exports the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da48f-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="da48f-117">-DatabaseName</span></span>
<span data-ttu-id="da48f-118">Указывает имя базы данных, из которой этот командлет экспортирует данные.</span><span class="sxs-lookup"><span data-stu-id="da48f-118">Specifies the name of the database from which this cmdlet exports data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da48f-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="da48f-119">-Profile</span></span>
<span data-ttu-id="da48f-120">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="da48f-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="da48f-121">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="da48f-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="da48f-122">-SqlConnectionContext</span><span class="sxs-lookup"><span data-stu-id="da48f-122">-SqlConnectionContext</span></span>
<span data-ttu-id="da48f-123">Задает контекст подключения для сервера, содержащего базу данных.</span><span class="sxs-lookup"><span data-stu-id="da48f-123">Specifies the connection context of a server that contains the database.</span></span>

```yaml
Type: ISqlServerConnectionInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da48f-124">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="da48f-124">-StorageContainer</span></span>
<span data-ttu-id="da48f-125">Указывает контейнер хранилища, содержащий большой двоичный объект, в который этот командлет экспортирует базу данных.</span><span class="sxs-lookup"><span data-stu-id="da48f-125">Specifies the storage container that contains the Blob into which this cmdlet export a database.</span></span>

```yaml
Type: AzureStorageContainer
Parameter Sets: ByContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da48f-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="da48f-126">-StorageContainerName</span></span>
<span data-ttu-id="da48f-127">Указывает имя контейнера хранилища, содержащего большой двоичный объект, в который этот командлет экспортирует базу данных.</span><span class="sxs-lookup"><span data-stu-id="da48f-127">Specifies the name of the storage container that contains the Blob into which this cmdlet exports a database.</span></span>

```yaml
Type: String
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da48f-128">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="da48f-128">-StorageContext</span></span>
<span data-ttu-id="da48f-129">Указывает контекст контейнера хранилища BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="da48f-129">Specifies the context of the Blob storage container.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da48f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da48f-130">CommonParameters</span></span>
<span data-ttu-id="da48f-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da48f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da48f-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da48f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da48f-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da48f-133">INPUTS</span></span>

## <span data-ttu-id="da48f-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da48f-134">OUTPUTS</span></span>

### <span data-ttu-id="da48f-135">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. ImportExportRequest</span><span class="sxs-lookup"><span data-stu-id="da48f-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="da48f-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="da48f-136">NOTES</span></span>

## <span data-ttu-id="da48f-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da48f-137">RELATED LINKS</span></span>

[<span data-ttu-id="da48f-138">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="da48f-138">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="da48f-139">Экспорт базы данных</span><span class="sxs-lookup"><span data-stu-id="da48f-139">Export Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781282.aspx)

[<span data-ttu-id="da48f-140">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="da48f-140">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="da48f-141">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="da48f-141">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="da48f-142">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="da48f-142">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


