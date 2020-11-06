---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: b78bcf228012edd022f9551a5834c61cebc8d278
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566394"
---
# <span data-ttu-id="bd3e1-101">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="bd3e1-101">Get-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="bd3e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd3e1-102">SYNOPSIS</span></span>
<span data-ttu-id="bd3e1-103">Получает параметры аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bd3e1-103">Gets the auditing settings of an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd3e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd3e1-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditing [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd3e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd3e1-105">DESCRIPTION</span></span>
<span data-ttu-id="bd3e1-106">Командлет **Get-AzureRmSqlDatabaseAuditing** получает параметры аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bd3e1-106">The **Get-AzureRmSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="bd3e1-107">Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="bd3e1-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="bd3e1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd3e1-108">EXAMPLES</span></span>

### <span data-ttu-id="bd3e1-109">Пример 1: получение параметров аудита для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="bd3e1-109">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

## <span data-ttu-id="bd3e1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd3e1-110">PARAMETERS</span></span>

### <span data-ttu-id="bd3e1-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bd3e1-111">-DatabaseName</span></span>
<span data-ttu-id="bd3e1-112">Имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="bd3e1-112">SQL Database name.</span></span>

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

### <span data-ttu-id="bd3e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd3e1-113">-DefaultProfile</span></span>
<span data-ttu-id="bd3e1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bd3e1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd3e1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd3e1-115">-ResourceGroupName</span></span>
<span data-ttu-id="bd3e1-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd3e1-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="bd3e1-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="bd3e1-117">-ServerName</span></span>
<span data-ttu-id="bd3e1-118">Имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="bd3e1-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="bd3e1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd3e1-119">-Confirm</span></span>
<span data-ttu-id="bd3e1-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bd3e1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd3e1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd3e1-121">-WhatIf</span></span>
<span data-ttu-id="bd3e1-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bd3e1-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd3e1-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bd3e1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd3e1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd3e1-124">CommonParameters</span></span>
<span data-ttu-id="bd3e1-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd3e1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd3e1-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd3e1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd3e1-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd3e1-127">INPUTS</span></span>

## <span data-ttu-id="bd3e1-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd3e1-128">OUTPUTS</span></span>

### <span data-ttu-id="bd3e1-129">Microsoft. Azure. Commands. SQL. Audit. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="bd3e1-129">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="bd3e1-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd3e1-130">NOTES</span></span>

## <span data-ttu-id="bd3e1-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd3e1-131">RELATED LINKS</span></span>
