---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
ms.openlocfilehash: 8ebe1cecc42d8ee01c270b994e1e10de4f402c1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563848"
---
# <span data-ttu-id="79dcc-101">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="79dcc-101">New-AzureRmSqlDatabaseImport</span></span>

## <span data-ttu-id="79dcc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79dcc-102">SYNOPSIS</span></span>
<span data-ttu-id="79dcc-103">Импортирует BACPAC-файл и создает на сервере новую базу данных.</span><span class="sxs-lookup"><span data-stu-id="79dcc-103">Imports a .bacpac file and create a new database on the server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79dcc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79dcc-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79dcc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79dcc-105">DESCRIPTION</span></span>
<span data-ttu-id="79dcc-106">Командлет **New-AzureRmSqlDatabaseImport** импортирует файл BACPAC из учетной записи хранения Azure в новую базу данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="79dcc-106">The **New-AzureRmSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="79dcc-107">Чтобы получить сведения о состоянии этого запроса, может быть отправлен запрос на получение состояния базы данных для импорта.</span><span class="sxs-lookup"><span data-stu-id="79dcc-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="79dcc-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79dcc-108">EXAMPLES</span></span>

### <span data-ttu-id="79dcc-109">Пример 1: Создание запроса на импорт для BACPAC-файла</span><span class="sxs-lookup"><span data-stu-id="79dcc-109">Example 1: Create an import request for a bacpac file</span></span>
```
PS C:\>New-AzureRmSqlDatabaseImport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword $SecureString -Edition Standard -ServiceObjectiveName S0 -DatabaseMaxSizeBytes 5000000
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="79dcc-110">Эта команда создает запрос на импорт для импорта BACPAC-пакета в новую базу данных.</span><span class="sxs-lookup"><span data-stu-id="79dcc-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="79dcc-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79dcc-111">PARAMETERS</span></span>

### <span data-ttu-id="79dcc-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="79dcc-112">-AdministratorLogin</span></span>
<span data-ttu-id="79dcc-113">Указывает имя администратора SQL.</span><span class="sxs-lookup"><span data-stu-id="79dcc-113">Specifies the name of the SQL administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dcc-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="79dcc-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="79dcc-115">Указывает пароль администратора SQL.</span><span class="sxs-lookup"><span data-stu-id="79dcc-115">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dcc-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="79dcc-116">-AuthenticationType</span></span>
<span data-ttu-id="79dcc-117">Указывает тип проверки подлинности, используемой для доступа к серверу.</span><span class="sxs-lookup"><span data-stu-id="79dcc-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="79dcc-118">Этот параметр по умолчанию имеет значение SQL, если не задан тип проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="79dcc-118">This parameter defaults to SQL if no authentication type is set.</span></span>

<span data-ttu-id="79dcc-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="79dcc-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79dcc-120">Microsoft.</span><span class="sxs-lookup"><span data-stu-id="79dcc-120">SQL.</span></span>
<span data-ttu-id="79dcc-121">Проверка подлинности SQL.</span><span class="sxs-lookup"><span data-stu-id="79dcc-121">SQL authentication.</span></span>
<span data-ttu-id="79dcc-122">Задайте для параметров *AdministratorLogin* и *AdministratorLoginPassword* имя пользователя и пароль администратора SQL.</span><span class="sxs-lookup"><span data-stu-id="79dcc-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="79dcc-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="79dcc-123">ADPassword.</span></span>
<span data-ttu-id="79dcc-124">Проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="79dcc-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="79dcc-125">Настройте *AdministratorLogin* и *AdministratorLoginPassword* на имя пользователя и пароль администратора Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="79dcc-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>

<span data-ttu-id="79dcc-126">Этот параметр доступен только на серверах SQL Database версии 12.</span><span class="sxs-lookup"><span data-stu-id="79dcc-126">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.AuthenticationType
Parameter Sets: (All)
Aliases: 
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dcc-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="79dcc-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="79dcc-128">Задает максимальный размер для новой импортированной базы данных.</span><span class="sxs-lookup"><span data-stu-id="79dcc-128">Specifies the maximum size for the newly imported database.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dcc-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="79dcc-129">-DatabaseName</span></span>
<span data-ttu-id="79dcc-130">Указывает имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="79dcc-130">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dcc-131">-Edition</span><span class="sxs-lookup"><span data-stu-id="79dcc-131">-Edition</span></span>
<span data-ttu-id="79dcc-132">Определяет версию новой базы данных, в которую будет импортироваться элемент.</span><span class="sxs-lookup"><span data-stu-id="79dcc-132">Specifies the edition of the new database to import to.</span></span>

<span data-ttu-id="79dcc-133">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="79dcc-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79dcc-134">Версию</span><span class="sxs-lookup"><span data-stu-id="79dcc-134">Premium</span></span>
- <span data-ttu-id="79dcc-135">Базового</span><span class="sxs-lookup"><span data-stu-id="79dcc-135">Basic</span></span>
- <span data-ttu-id="79dcc-136">Стандартная</span><span class="sxs-lookup"><span data-stu-id="79dcc-136">Standard</span></span>
- <span data-ttu-id="79dcc-137">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="79dcc-137">DataWarehouse</span></span>
- <span data-ttu-id="79dcc-138">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="79dcc-138">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dcc-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79dcc-139">-ResourceGroupName</span></span>
<span data-ttu-id="79dcc-140">Указывает имя группы ресурсов для сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="79dcc-140">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="79dcc-141">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="79dcc-141">-ServerName</span></span>
<span data-ttu-id="79dcc-142">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="79dcc-142">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="79dcc-143">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="79dcc-143">-ServiceObjectiveName</span></span>
<span data-ttu-id="79dcc-144">Указывает имя цели обслуживания, которую нужно назначить базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="79dcc-144">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dcc-145">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="79dcc-145">-StorageKey</span></span>
<span data-ttu-id="79dcc-146">Задает клавишу доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="79dcc-146">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dcc-147">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="79dcc-147">-StorageKeyType</span></span>
<span data-ttu-id="79dcc-148">Указывает тип клавиши доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="79dcc-148">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="79dcc-149">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="79dcc-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79dcc-150">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="79dcc-150">StorageAccessKey.</span></span>
<span data-ttu-id="79dcc-151">Использует ключ учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="79dcc-151">Uses the storage account key.</span></span> 
- <span data-ttu-id="79dcc-152">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="79dcc-152">SharedAccessKey.</span></span>
<span data-ttu-id="79dcc-153">Использует ключ подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="79dcc-153">Uses the Shared Access Signature (SAS) key.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.StorageKeyType
Parameter Sets: (All)
Aliases: 
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dcc-154">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="79dcc-154">-StorageUri</span></span>
<span data-ttu-id="79dcc-155">Указывает URI BLOB-объектов для BACPAC-файла.</span><span class="sxs-lookup"><span data-stu-id="79dcc-155">Specifies the blob URI of the .bacpac file.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dcc-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79dcc-156">-Confirm</span></span>
<span data-ttu-id="79dcc-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="79dcc-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79dcc-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79dcc-158">-WhatIf</span></span>
<span data-ttu-id="79dcc-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="79dcc-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79dcc-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="79dcc-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79dcc-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79dcc-161">-DefaultProfile</span></span>
<span data-ttu-id="79dcc-162">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79dcc-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79dcc-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79dcc-163">CommonParameters</span></span>
<span data-ttu-id="79dcc-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79dcc-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79dcc-165">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79dcc-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79dcc-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79dcc-166">INPUTS</span></span>

## <span data-ttu-id="79dcc-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79dcc-167">OUTPUTS</span></span>

### <span data-ttu-id="79dcc-168">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="79dcc-168">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="79dcc-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="79dcc-169">NOTES</span></span>
* <span data-ttu-id="79dcc-170">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, база данных и MSSQL</span><span class="sxs-lookup"><span data-stu-id="79dcc-170">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="79dcc-171">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79dcc-171">RELATED LINKS</span></span>

[<span data-ttu-id="79dcc-172">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="79dcc-172">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="79dcc-173">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="79dcc-173">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="79dcc-174">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="79dcc-174">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

