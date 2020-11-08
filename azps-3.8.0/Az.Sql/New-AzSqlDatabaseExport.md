---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: 2b7722ab8ca60c88e5ee9771b3f25526f6410fa4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065218"
---
# <span data-ttu-id="151fb-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="151fb-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="151fb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="151fb-102">SYNOPSIS</span></span>
<span data-ttu-id="151fb-103">Экспортирует базу данных SQL Azure в виде BACPAC-файла в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="151fb-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="151fb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="151fb-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="151fb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="151fb-105">DESCRIPTION</span></span>
<span data-ttu-id="151fb-106">Командлет **New-AzSqlDatabaseExport** экспортирует базу данных SQL Azure в виде BACPAC-файла в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="151fb-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="151fb-107">Чтобы получить сведения о состоянии этого запроса, может быть отправлен запрос на получение состояния базы данных для экспорта.</span><span class="sxs-lookup"><span data-stu-id="151fb-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="151fb-108">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="151fb-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="151fb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="151fb-109">EXAMPLES</span></span>

### <span data-ttu-id="151fb-110">Пример 1: Создание запроса на экспорт для базы данных</span><span class="sxs-lookup"><span data-stu-id="151fb-110">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
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

<span data-ttu-id="151fb-111">Эта команда создает запрос на экспорт для указанной базы данных.</span><span class="sxs-lookup"><span data-stu-id="151fb-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="151fb-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="151fb-112">PARAMETERS</span></span>

### <span data-ttu-id="151fb-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="151fb-113">-AdministratorLogin</span></span>
<span data-ttu-id="151fb-114">Указывает имя администратора SQL.</span><span class="sxs-lookup"><span data-stu-id="151fb-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="151fb-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="151fb-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="151fb-116">Указывает пароль администратора SQL.</span><span class="sxs-lookup"><span data-stu-id="151fb-116">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="151fb-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="151fb-117">-AuthenticationType</span></span>
<span data-ttu-id="151fb-118">Указывает тип проверки подлинности, используемой для доступа к серверу.</span><span class="sxs-lookup"><span data-stu-id="151fb-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="151fb-119">Если тип проверки подлинности не задан, значение по умолчанию — SQL.</span><span class="sxs-lookup"><span data-stu-id="151fb-119">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="151fb-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="151fb-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="151fb-121">Microsoft.</span><span class="sxs-lookup"><span data-stu-id="151fb-121">Sql.</span></span>
<span data-ttu-id="151fb-122">Проверка подлинности SQL.</span><span class="sxs-lookup"><span data-stu-id="151fb-122">SQL authentication.</span></span>
<span data-ttu-id="151fb-123">Задайте для свойства *AdministratorLogin* и *AdministratorLoginPassword* имя пользователя и пароль администратора SQL.</span><span class="sxs-lookup"><span data-stu-id="151fb-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="151fb-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="151fb-124">ADPassword.</span></span>
<span data-ttu-id="151fb-125">Проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="151fb-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="151fb-126">Укажите имя пользователя и пароль администратора Azure AD в *AdministratorLogin* и *AdministratorLoginPassword* .</span><span class="sxs-lookup"><span data-stu-id="151fb-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="151fb-127">Этот параметр доступен только на серверах SQL Database версии 12.</span><span class="sxs-lookup"><span data-stu-id="151fb-127">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="151fb-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="151fb-128">-DatabaseName</span></span>
<span data-ttu-id="151fb-129">Указывает имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="151fb-129">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="151fb-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="151fb-130">-DefaultProfile</span></span>
<span data-ttu-id="151fb-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="151fb-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="151fb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="151fb-132">-ResourceGroupName</span></span>
<span data-ttu-id="151fb-133">Указывает имя группы ресурсов для сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="151fb-133">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="151fb-134">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="151fb-134">-ServerName</span></span>
<span data-ttu-id="151fb-135">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="151fb-135">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="151fb-136">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="151fb-136">-StorageKey</span></span>
<span data-ttu-id="151fb-137">Задает клавишу доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="151fb-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="151fb-138">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="151fb-138">-StorageKeyType</span></span>
<span data-ttu-id="151fb-139">Указывает тип клавиши доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="151fb-139">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="151fb-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="151fb-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="151fb-141">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="151fb-141">StorageAccessKey.</span></span>
<span data-ttu-id="151fb-142">Это значение использует ключ учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="151fb-142">This value uses a storage account key.</span></span> 
- <span data-ttu-id="151fb-143">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="151fb-143">SharedAccessKey.</span></span>
<span data-ttu-id="151fb-144">Это значение использует ключ подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="151fb-144">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="151fb-145">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="151fb-145">-StorageUri</span></span>
<span data-ttu-id="151fb-146">Указывает ссылку на большой двоичный объект в виде URL-адреса на файл. BACPAC.</span><span class="sxs-lookup"><span data-stu-id="151fb-146">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="151fb-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="151fb-147">-Confirm</span></span>
<span data-ttu-id="151fb-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="151fb-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="151fb-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="151fb-149">-WhatIf</span></span>
<span data-ttu-id="151fb-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="151fb-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="151fb-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="151fb-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="151fb-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="151fb-152">CommonParameters</span></span>
<span data-ttu-id="151fb-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="151fb-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="151fb-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="151fb-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="151fb-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="151fb-155">INPUTS</span></span>

### <span data-ttu-id="151fb-156">System. String</span><span class="sxs-lookup"><span data-stu-id="151fb-156">System.String</span></span>

## <span data-ttu-id="151fb-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="151fb-157">OUTPUTS</span></span>

### <span data-ttu-id="151fb-158">Microsoft. Azure. Commands. SQL. ImportExport. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="151fb-158">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="151fb-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="151fb-159">NOTES</span></span>
* <span data-ttu-id="151fb-160">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, база данных и MSSQL</span><span class="sxs-lookup"><span data-stu-id="151fb-160">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="151fb-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="151fb-161">RELATED LINKS</span></span>

[<span data-ttu-id="151fb-162">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="151fb-162">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="151fb-163">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="151fb-163">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="151fb-164">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="151fb-164">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
