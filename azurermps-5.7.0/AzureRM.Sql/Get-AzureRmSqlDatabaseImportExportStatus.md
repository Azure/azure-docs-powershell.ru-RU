---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
ms.openlocfilehash: 9a1c56f528b9865e1a68e74d35885fc6f8b24bf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557084"
---
# <span data-ttu-id="aa847-101">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="aa847-101">Get-AzureRmSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="aa847-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa847-102">SYNOPSIS</span></span>
<span data-ttu-id="aa847-103">Получает подробные сведения о импорте или экспорте базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="aa847-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa847-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa847-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseImportExportStatus [-OperationStatusLink] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa847-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa847-105">DESCRIPTION</span></span>
<span data-ttu-id="aa847-106">Командлет **Get-AzureRmSqlDatabaseImportExportStatus** получает сведения о файле BACPAC — импорт из учетной записи хранения в базу данных Azure SQL или экспорт базы данных SQL Azure в качестве BACPAC-файла в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="aa847-106">The **Get-AzureRmSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>

<span data-ttu-id="aa847-107">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="aa847-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="aa847-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa847-108">EXAMPLES</span></span>

### <span data-ttu-id="aa847-109">Пример 1: получение состояния импорта и экспорта базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="aa847-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="aa847-110">Эта команда возвращает состояние запроса на импорт или экспорт для базы данных по указанному URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="aa847-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="aa847-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa847-111">PARAMETERS</span></span>

### <span data-ttu-id="aa847-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa847-112">-DefaultProfile</span></span>
<span data-ttu-id="aa847-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="aa847-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa847-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="aa847-114">-OperationStatusLink</span></span>
<span data-ttu-id="aa847-115">Указывает ссылку на состояние, возвращаемую командлетами New-AzureRmSqlDatabaseExport и New-AzureRmSqlDatabaseImport.</span><span class="sxs-lookup"><span data-stu-id="aa847-115">Specifies the status link that is returned from the New-AzureRmSqlDatabaseExport or New-AzureRmSqlDatabaseImport cmdlets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa847-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa847-116">-Confirm</span></span>
<span data-ttu-id="aa847-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aa847-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa847-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa847-118">-WhatIf</span></span>
<span data-ttu-id="aa847-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aa847-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa847-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aa847-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa847-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa847-121">CommonParameters</span></span>
<span data-ttu-id="aa847-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa847-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa847-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa847-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa847-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa847-124">INPUTS</span></span>

### <span data-ttu-id="aa847-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="aa847-125">None</span></span>
<span data-ttu-id="aa847-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="aa847-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aa847-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa847-127">OUTPUTS</span></span>

## <span data-ttu-id="aa847-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa847-128">NOTES</span></span>
* <span data-ttu-id="aa847-129">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, база данных и MSSQL</span><span class="sxs-lookup"><span data-stu-id="aa847-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="aa847-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa847-130">RELATED LINKS</span></span>

[<span data-ttu-id="aa847-131">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="aa847-131">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="aa847-132">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="aa847-132">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="aa847-133">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="aa847-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
