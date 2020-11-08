---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5EE936CA-DD9A-4BC6-B835-E22AE633B46D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc7c8f39f1bdbd35cfffeb59b3b4f184f30845e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075427"
---
# <span data-ttu-id="02a1b-101">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="02a1b-101">Start-AzureSqlDatabaseImport</span></span>

## <span data-ttu-id="02a1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="02a1b-103">Запускает операцию импорта из хранилища BLOB-объектов в базу данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="02a1b-103">Starts an import operation from blob storage to an Azure SQL Database.</span></span>

## <span data-ttu-id="02a1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02a1b-104">SYNTAX</span></span>

### <span data-ttu-id="02a1b-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="02a1b-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="02a1b-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="02a1b-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="02a1b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02a1b-107">DESCRIPTION</span></span>
<span data-ttu-id="02a1b-108">Командлет **Start-AzureSqlDatabaseImport** запускает операцию импорта из хранилища BLOB-объектов Azure в базу данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="02a1b-108">The **Start-AzureSqlDatabaseImport** cmdlet starts an import operation from Azure Blob storage to an Azure SQL Database.</span></span>
<span data-ttu-id="02a1b-109">Если база данных не существует, этот командлет создает его с использованием указанных значений размера и выпуска.</span><span class="sxs-lookup"><span data-stu-id="02a1b-109">If the database does not exist, this cmdlet creates it by using the size and edition values that you specify.</span></span>
<span data-ttu-id="02a1b-110">Для операции требуется контекст подключения к серверу базы данных.</span><span class="sxs-lookup"><span data-stu-id="02a1b-110">The operation requires a database server connection context.</span></span>
<span data-ttu-id="02a1b-111">Используйте командлет Get-AzureSqlDatabaseImportExportStatus, чтобы получить состояние операции импорта.</span><span class="sxs-lookup"><span data-stu-id="02a1b-111">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the import operation.</span></span>

## <span data-ttu-id="02a1b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02a1b-112">EXAMPLES</span></span>

### <span data-ttu-id="02a1b-113">Пример 1: импорт базы данных</span><span class="sxs-lookup"><span data-stu-id="02a1b-113">Example 1: Import a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credentials $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $ImportRequest = Start-AzureSqlDatabaseImport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="02a1b-114">В этом примере инициируется процесс импорта из хранилища BLOB-объектов в переменной $BlobName в базу данных SQL Azure с именем DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="02a1b-114">This example initiates an import process from the Blob storage in the $BlobName variable into the Azure SQL Database named DatabaseName.</span></span>

## <span data-ttu-id="02a1b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02a1b-115">PARAMETERS</span></span>

### <span data-ttu-id="02a1b-116">-BlobName</span><span class="sxs-lookup"><span data-stu-id="02a1b-116">-BlobName</span></span>
<span data-ttu-id="02a1b-117">Указывает имя хранилища BLOB-объектов Azure, из которого этот командлет импортирует базу данных.</span><span class="sxs-lookup"><span data-stu-id="02a1b-117">Specifies the name of the Azure Blob storage from which this cmdlet imports the database.</span></span>

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

### <span data-ttu-id="02a1b-118">-DatabaseMaxSize</span><span class="sxs-lookup"><span data-stu-id="02a1b-118">-DatabaseMaxSize</span></span>
<span data-ttu-id="02a1b-119">Задает максимальный размер базы данных (в гигабайтах).</span><span class="sxs-lookup"><span data-stu-id="02a1b-119">Specifies the maximum size, in gigabytes, for the database.</span></span>
<span data-ttu-id="02a1b-120">Если база данных не существует, этот командлет создает ее на основе этого максимального размера.</span><span class="sxs-lookup"><span data-stu-id="02a1b-120">If the database does not exist, this cmdlet creates it based on this maximum size.</span></span>
<span data-ttu-id="02a1b-121">Приемлемые значения зависят от выпуска.</span><span class="sxs-lookup"><span data-stu-id="02a1b-121">The acceptable values differ based on edition.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a1b-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="02a1b-122">-DatabaseName</span></span>
<span data-ttu-id="02a1b-123">Задает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="02a1b-123">Specifies a name for the database.</span></span>
<span data-ttu-id="02a1b-124">Если база данных не существует, этот командлет создает его и назначает имя, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="02a1b-124">If the database does not exist, this cmdlet creates it, and assigns the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="02a1b-125">-Edition</span><span class="sxs-lookup"><span data-stu-id="02a1b-125">-Edition</span></span>
<span data-ttu-id="02a1b-126">Указывает версию базы данных.</span><span class="sxs-lookup"><span data-stu-id="02a1b-126">Specifies the edition of the database.</span></span>
<span data-ttu-id="02a1b-127">Если база данных не существует, этот командлет создаст его в качестве этого выпуска.</span><span class="sxs-lookup"><span data-stu-id="02a1b-127">If the database does not exist, this cmdlet creates it as this edition.</span></span>
<span data-ttu-id="02a1b-128">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="02a1b-128">Valid values are:</span></span> 

- <span data-ttu-id="02a1b-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="02a1b-129">None</span></span>
- <span data-ttu-id="02a1b-130">Сайта</span><span class="sxs-lookup"><span data-stu-id="02a1b-130">Web</span></span> 
- <span data-ttu-id="02a1b-131">Деловы</span><span class="sxs-lookup"><span data-stu-id="02a1b-131">Business</span></span> 
- <span data-ttu-id="02a1b-132">Базового</span><span class="sxs-lookup"><span data-stu-id="02a1b-132">Basic</span></span>
- <span data-ttu-id="02a1b-133">Стандартная</span><span class="sxs-lookup"><span data-stu-id="02a1b-133">Standard</span></span>
- <span data-ttu-id="02a1b-134">Версию</span><span class="sxs-lookup"><span data-stu-id="02a1b-134">Premium</span></span>

<span data-ttu-id="02a1b-135">По умолчанию используется веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="02a1b-135">The default is Web.</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a1b-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="02a1b-136">-Profile</span></span>
<span data-ttu-id="02a1b-137">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="02a1b-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="02a1b-138">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="02a1b-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="02a1b-139">-SqlConnectionContext</span><span class="sxs-lookup"><span data-stu-id="02a1b-139">-SqlConnectionContext</span></span>
<span data-ttu-id="02a1b-140">Задает контекст подключения для сервера, содержащего базу данных.</span><span class="sxs-lookup"><span data-stu-id="02a1b-140">Specifies the connection context of a server that contains the database.</span></span>

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

### <span data-ttu-id="02a1b-141">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="02a1b-141">-StorageContainer</span></span>
<span data-ttu-id="02a1b-142">Указывает контейнер хранилища, содержащий большой двоичный объект, из которого этот командлет импортирует базу данных.</span><span class="sxs-lookup"><span data-stu-id="02a1b-142">Specifies the storage container that contains the Blob from which this cmdlet imports a database.</span></span>

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

### <span data-ttu-id="02a1b-143">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="02a1b-143">-StorageContainerName</span></span>
<span data-ttu-id="02a1b-144">Указывает имя контейнера хранилища BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="02a1b-144">Specifies the name of the Blob storage container.</span></span>

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

### <span data-ttu-id="02a1b-145">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="02a1b-145">-StorageContext</span></span>
<span data-ttu-id="02a1b-146">Указывает контекст контейнера хранилища BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="02a1b-146">Specifies the context of the Blob storage container.</span></span>

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

### <span data-ttu-id="02a1b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a1b-147">CommonParameters</span></span>
<span data-ttu-id="02a1b-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02a1b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a1b-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02a1b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a1b-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02a1b-150">INPUTS</span></span>

## <span data-ttu-id="02a1b-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02a1b-151">OUTPUTS</span></span>

### <span data-ttu-id="02a1b-152">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. ImportExportRequest</span><span class="sxs-lookup"><span data-stu-id="02a1b-152">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="02a1b-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="02a1b-153">NOTES</span></span>

## <span data-ttu-id="02a1b-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02a1b-154">RELATED LINKS</span></span>

[<span data-ttu-id="02a1b-155">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="02a1b-155">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="02a1b-156">Импорт базы данных</span><span class="sxs-lookup"><span data-stu-id="02a1b-156">Import Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781284.aspx)

[<span data-ttu-id="02a1b-157">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="02a1b-157">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="02a1b-158">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="02a1b-158">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="02a1b-159">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="02a1b-159">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)


