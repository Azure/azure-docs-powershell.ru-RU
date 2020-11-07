---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: 4d15400da4105f719f5948a53512f6c33cbd3bd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733538"
---
# <span data-ttu-id="7db65-101">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="7db65-101">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="7db65-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7db65-102">SYNOPSIS</span></span>
<span data-ttu-id="7db65-103">Возвращает политику аудита для базы данных.</span><span class="sxs-lookup"><span data-stu-id="7db65-103">Gets the auditing policy of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7db65-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7db65-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7db65-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7db65-105">DESCRIPTION</span></span>
<span data-ttu-id="7db65-106">Командлет **Get-AzureRmSqlDatabaseAuditingPolicy** получает политику аудита для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7db65-106">The **Get-AzureRmSqlDatabaseAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL Database.</span></span>
<span data-ttu-id="7db65-107">Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="7db65-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="7db65-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7db65-108">EXAMPLES</span></span>

### <span data-ttu-id="7db65-109">Пример 1: получение политики аудита для базы данных SQL Azure с определенными для него разаудитом</span><span class="sxs-lookup"><span data-stu-id="7db65-109">Example 1: Get the auditing policy of an Azure SQL database with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
UseServerDefault       : Disabled
EventType              : {PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure...} 
TableIdentifier        : MyAuditTableName
FullAuditLogsTableName : SQLDBAuditLogsMyAuditTableName
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Table
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

### <span data-ttu-id="7db65-110">Пример 2: получение политики аудита для базы данных Azure SQL с определенными аудитом больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="7db65-110">Example 2: Get the auditing policy of an Azure SQL database with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
AuditAction            : {}
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...} 
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Blob
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="7db65-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7db65-111">PARAMETERS</span></span>

### <span data-ttu-id="7db65-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7db65-112">-DatabaseName</span></span>
<span data-ttu-id="7db65-113">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="7db65-113">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7db65-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7db65-114">-DefaultProfile</span></span>
<span data-ttu-id="7db65-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7db65-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7db65-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7db65-116">-ResourceGroupName</span></span>
<span data-ttu-id="7db65-117">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="7db65-117">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="7db65-118">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="7db65-118">-ServerName</span></span>
<span data-ttu-id="7db65-119">Указывает имя сервера, на котором находится база данных.</span><span class="sxs-lookup"><span data-stu-id="7db65-119">Specifies the name of the server where the database is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7db65-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7db65-120">-Confirm</span></span>
<span data-ttu-id="7db65-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7db65-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7db65-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7db65-122">-WhatIf</span></span>
<span data-ttu-id="7db65-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7db65-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7db65-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7db65-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7db65-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7db65-125">CommonParameters</span></span>
<span data-ttu-id="7db65-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7db65-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7db65-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7db65-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7db65-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7db65-128">INPUTS</span></span>

### <span data-ttu-id="7db65-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="7db65-129">None</span></span>
<span data-ttu-id="7db65-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7db65-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7db65-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7db65-131">OUTPUTS</span></span>

### <span data-ttu-id="7db65-132">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="7db65-132">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="7db65-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="7db65-133">NOTES</span></span>

## <span data-ttu-id="7db65-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7db65-134">RELATED LINKS</span></span>

[<span data-ttu-id="7db65-135">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="7db65-135">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="7db65-136">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="7db65-136">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)



