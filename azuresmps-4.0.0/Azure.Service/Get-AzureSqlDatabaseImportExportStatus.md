---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076294"
---
# <span data-ttu-id="b1134-101">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="b1134-101">Get-AzureSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="b1134-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1134-102">SYNOPSIS</span></span>
<span data-ttu-id="b1134-103">Возвращает состояние запроса на импорт или экспорт.</span><span class="sxs-lookup"><span data-stu-id="b1134-103">Gets the status of an import or export request.</span></span>

## <span data-ttu-id="b1134-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1134-104">SYNTAX</span></span>

### <span data-ttu-id="b1134-105">ByConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="b1134-105">ByConnectionInfo</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b1134-106">ByRequestObject</span><span class="sxs-lookup"><span data-stu-id="b1134-106">ByRequestObject</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1134-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1134-107">DESCRIPTION</span></span>
<span data-ttu-id="b1134-108">Командлет **Get-AzureSqlDatabaseImportExportStatus** получает состояние запроса на импорт или экспорт.</span><span class="sxs-lookup"><span data-stu-id="b1134-108">The **Get-AzureSqlDatabaseImportExportStatus** cmdlet gets the status of an import or export request.</span></span>
<span data-ttu-id="b1134-109">Командлет Start-AzureSqlDatabaseImport или Start-AzureSqlDatabaseExport инициирует запросы.</span><span class="sxs-lookup"><span data-stu-id="b1134-109">The Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet initiates requests.</span></span>
<span data-ttu-id="b1134-110">Вы можете задать объект Request с помощью параметра *request* или определить запрос с помощью параметра *RequestId* и *имени пользователя* , *пароля* и *сервера* доменных параметров.</span><span class="sxs-lookup"><span data-stu-id="b1134-110">You can specify the request object by using the *Request* parameter, or you can identify the request by using the *RequestId* parameter and the *Username* , *Password* , and *ServerName* parameters.</span></span>

## <span data-ttu-id="b1134-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1134-111">EXAMPLES</span></span>

### <span data-ttu-id="b1134-112">Пример 1: получение состояния запроса на экспорт</span><span class="sxs-lookup"><span data-stu-id="b1134-112">Example 1: Get the status of an export request</span></span>
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

<span data-ttu-id="b1134-113">Первая команда создает запрос на экспорт, а затем сохраняет его в переменной $ExportRequest.</span><span class="sxs-lookup"><span data-stu-id="b1134-113">The first command creates an export request, and then stores it in the $ExportRequest variable.</span></span>

<span data-ttu-id="b1134-114">Вторая команда возвращает состояние запроса на экспорт, который хранится в $ExportRequest.</span><span class="sxs-lookup"><span data-stu-id="b1134-114">The second command gets the status of the export request stored in $ExportRequest.</span></span>

## <span data-ttu-id="b1134-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1134-115">PARAMETERS</span></span>

### <span data-ttu-id="b1134-116">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="b1134-116">-Password</span></span>
<span data-ttu-id="b1134-117">Указывает пароль, необходимый для подключения к серверу базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b1134-117">Specifies the password that is required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="b1134-118">Вы должны указать этот параметр, если вы указали параметр *RequestId* .</span><span class="sxs-lookup"><span data-stu-id="b1134-118">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1134-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="b1134-119">-Profile</span></span>
<span data-ttu-id="b1134-120">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b1134-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b1134-121">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b1134-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b1134-122">-Request</span><span class="sxs-lookup"><span data-stu-id="b1134-122">-Request</span></span>
<span data-ttu-id="b1134-123">Указывает объект **ImportExportRequest** .</span><span class="sxs-lookup"><span data-stu-id="b1134-123">Specifies an **ImportExportRequest** object.</span></span>
<span data-ttu-id="b1134-124">Чтобы получить объект запроса на импорт или экспорт, используйте командлет Start-AzureSqlDatabaseImport или Start-AzureSqlDatabaseExport.</span><span class="sxs-lookup"><span data-stu-id="b1134-124">To obtain an import or export request object, use the Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet.</span></span>

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1134-125">-RequestId</span><span class="sxs-lookup"><span data-stu-id="b1134-125">-RequestId</span></span>
<span data-ttu-id="b1134-126">Указывает GUID операции импорта или экспорта, для которой этот командлет получает состояние.</span><span class="sxs-lookup"><span data-stu-id="b1134-126">Specifies the GUID of the import or export operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="b1134-127">Если указан этот параметр, необходимо указать *имя пользователя* , *пароль* и *имя сервера* .</span><span class="sxs-lookup"><span data-stu-id="b1134-127">If you specify this parameter, you must specify the *UserName* , *Password* , and *ServerName* parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1134-128">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="b1134-128">-ServerName</span></span>
<span data-ttu-id="b1134-129">Указывает имя сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b1134-129">Specifies the name of the Azure SQL Database server.</span></span>
<span data-ttu-id="b1134-130">Вы должны указать этот параметр, если вы указали параметр *RequestId* .</span><span class="sxs-lookup"><span data-stu-id="b1134-130">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1134-131">-Username</span><span class="sxs-lookup"><span data-stu-id="b1134-131">-Username</span></span>
<span data-ttu-id="b1134-132">Указывает имя пользователя, необходимое для подключения к серверу базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b1134-132">Specifies the user name required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="b1134-133">Вы должны указать этот параметр, если вы указали параметр *RequestId* .</span><span class="sxs-lookup"><span data-stu-id="b1134-133">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1134-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1134-134">CommonParameters</span></span>
<span data-ttu-id="b1134-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1134-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1134-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1134-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1134-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1134-137">INPUTS</span></span>

## <span data-ttu-id="b1134-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1134-138">OUTPUTS</span></span>

### <span data-ttu-id="b1134-139">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. ImportExport. StatusInfo</span><span class="sxs-lookup"><span data-stu-id="b1134-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExport.StatusInfo</span></span>

## <span data-ttu-id="b1134-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1134-140">NOTES</span></span>

## <span data-ttu-id="b1134-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1134-141">RELATED LINKS</span></span>

[<span data-ttu-id="b1134-142">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="b1134-142">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="b1134-143">Получение состояния импорта базы данных экспорта</span><span class="sxs-lookup"><span data-stu-id="b1134-143">Get Import Export Database Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[<span data-ttu-id="b1134-144">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="b1134-144">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="b1134-145">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="b1134-145">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)

[<span data-ttu-id="b1134-146">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="b1134-146">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


