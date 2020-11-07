---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
ms.openlocfilehash: 838c09c8a86c081a1b335fa22f4473d099a1b182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734102"
---
# <span data-ttu-id="3e6e7-101">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="3e6e7-101">New-AzureRmSqlDatabaseExport</span></span>

## <span data-ttu-id="3e6e7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e6e7-102">SYNOPSIS</span></span>
<span data-ttu-id="3e6e7-103">Экспортирует базу данных SQL Azure в виде BACPAC-файла в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e6e7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e6e7-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e6e7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e6e7-105">DESCRIPTION</span></span>
<span data-ttu-id="3e6e7-106">Командлет **New-AzureRmSqlDatabaseExport** экспортирует базу данных SQL Azure в виде BACPAC-файла в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-106">The **New-AzureRmSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="3e6e7-107">Чтобы получить сведения о состоянии этого запроса, может быть отправлен запрос на получение состояния базы данных для экспорта.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="3e6e7-108">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3e6e7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e6e7-109">EXAMPLES</span></span>

### <span data-ttu-id="3e6e7-110">Пример 1: Создание запроса на экспорт для базы данных</span><span class="sxs-lookup"><span data-stu-id="3e6e7-110">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.azure.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="3e6e7-111">Эта команда создает запрос на экспорт для указанной базы данных.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="3e6e7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e6e7-112">PARAMETERS</span></span>

### <span data-ttu-id="3e6e7-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="3e6e7-113">-AdministratorLogin</span></span>
<span data-ttu-id="3e6e7-114">Указывает имя администратора SQL.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="3e6e7-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="3e6e7-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="3e6e7-116">Указывает пароль администратора SQL.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-116">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="3e6e7-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="3e6e7-117">-AuthenticationType</span></span>
<span data-ttu-id="3e6e7-118">Указывает тип проверки подлинности, используемой для доступа к серверу.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="3e6e7-119">Если тип проверки подлинности не задан, значение по умолчанию — SQL.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-119">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="3e6e7-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3e6e7-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3e6e7-121">Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-121">Sql.</span></span>
<span data-ttu-id="3e6e7-122">Проверка подлинности SQL.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-122">SQL authentication.</span></span>
<span data-ttu-id="3e6e7-123">Задайте для свойства *AdministratorLogin* и *AdministratorLoginPassword* имя пользователя и пароль администратора SQL.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="3e6e7-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-124">ADPassword.</span></span>
<span data-ttu-id="3e6e7-125">Проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="3e6e7-126">Укажите имя пользователя и пароль администратора Azure AD в *AdministratorLogin* и *AdministratorLoginPassword* .</span><span class="sxs-lookup"><span data-stu-id="3e6e7-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="3e6e7-127">Этот параметр доступен только на серверах SQL Database версии 12.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-127">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="3e6e7-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3e6e7-128">-DatabaseName</span></span>
<span data-ttu-id="3e6e7-129">Указывает имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-129">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="3e6e7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e6e7-130">-DefaultProfile</span></span>
<span data-ttu-id="3e6e7-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3e6e7-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e6e7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e6e7-132">-ResourceGroupName</span></span>
<span data-ttu-id="3e6e7-133">Указывает имя группы ресурсов для сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-133">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="3e6e7-134">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="3e6e7-134">-ServerName</span></span>
<span data-ttu-id="3e6e7-135">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-135">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="3e6e7-136">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="3e6e7-136">-StorageKey</span></span>
<span data-ttu-id="3e6e7-137">Задает клавишу доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="3e6e7-138">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="3e6e7-138">-StorageKeyType</span></span>
<span data-ttu-id="3e6e7-139">Указывает тип клавиши доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-139">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="3e6e7-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3e6e7-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3e6e7-141">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-141">StorageAccessKey.</span></span>
<span data-ttu-id="3e6e7-142">Это значение использует ключ учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-142">This value uses a storage account key.</span></span> 
- <span data-ttu-id="3e6e7-143">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-143">SharedAccessKey.</span></span>
<span data-ttu-id="3e6e7-144">Это значение использует ключ подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="3e6e7-144">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="3e6e7-145">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="3e6e7-145">-StorageUri</span></span>
<span data-ttu-id="3e6e7-146">Указывает ссылку на большой двоичный объект в виде URL-адреса на файл. BACPAC.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-146">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="3e6e7-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e6e7-147">-Confirm</span></span>
<span data-ttu-id="3e6e7-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e6e7-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e6e7-149">-WhatIf</span></span>
<span data-ttu-id="3e6e7-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e6e7-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e6e7-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e6e7-152">CommonParameters</span></span>
<span data-ttu-id="3e6e7-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e6e7-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e6e7-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e6e7-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e6e7-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e6e7-155">INPUTS</span></span>

### <span data-ttu-id="3e6e7-156">System. String</span><span class="sxs-lookup"><span data-stu-id="3e6e7-156">System.String</span></span>

## <span data-ttu-id="3e6e7-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e6e7-157">OUTPUTS</span></span>

### <span data-ttu-id="3e6e7-158">Microsoft. Azure. Commands. SQL. ImportExport. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="3e6e7-158">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="3e6e7-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e6e7-159">NOTES</span></span>
* <span data-ttu-id="3e6e7-160">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, база данных и MSSQL</span><span class="sxs-lookup"><span data-stu-id="3e6e7-160">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="3e6e7-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e6e7-161">RELATED LINKS</span></span>

[<span data-ttu-id="3e6e7-162">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="3e6e7-162">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="3e6e7-163">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="3e6e7-163">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="3e6e7-164">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="3e6e7-164">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
