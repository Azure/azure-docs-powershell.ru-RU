---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: af2f10b371eb21558a4b675331ec97f797611d26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562520"
---
# <span data-ttu-id="a0f02-101">Stop-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="a0f02-101">Stop-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="a0f02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a0f02-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f02-103">Отменяет операцию асинхронных обновлений для базы данных.</span><span class="sxs-lookup"><span data-stu-id="a0f02-103">Cancels the asynchronous updates operation on the database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0f02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a0f02-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0f02-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0f02-105">DESCRIPTION</span></span>
<span data-ttu-id="a0f02-106">Командлет **Stop-AzureRmSqlDatabaseActivity** отменяет операцию асинхронных обновлений для базы данных.</span><span class="sxs-lookup"><span data-stu-id="a0f02-106">The **Stop-AzureRmSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="a0f02-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a0f02-107">EXAMPLES</span></span>

### <span data-ttu-id="a0f02-108">Пример 1: отмена операции асинхронных обновлений для базы данных</span><span class="sxs-lookup"><span data-stu-id="a0f02-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : Database01
State           : CANCELLED
Operation       : UpdateLogicalDatabase
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete : 
Properties      : Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel+DatabaseState
```

<span data-ttu-id="a0f02-109">Эта команда отменяет операцию асинхронных обновлений для базы данных.</span><span class="sxs-lookup"><span data-stu-id="a0f02-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="a0f02-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a0f02-110">PARAMETERS</span></span>

### <span data-ttu-id="a0f02-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a0f02-111">-DatabaseName</span></span>
<span data-ttu-id="a0f02-112">Указывает имя базы данных, для которой этот командлет получает состояние.</span><span class="sxs-lookup"><span data-stu-id="a0f02-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f02-113">-DefaultProfile</span></span>
<span data-ttu-id="a0f02-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0f02-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0f02-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a0f02-115">-ElasticPoolName</span></span>
<span data-ttu-id="a0f02-116">Имя пула эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a0f02-116">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f02-117">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="a0f02-117">-OperationId</span></span>
<span data-ttu-id="a0f02-118">Указывает идентификатор операции, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a0f02-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f02-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f02-119">-ResourceGroupName</span></span>
<span data-ttu-id="a0f02-120">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="a0f02-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a0f02-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="a0f02-121">-ServerName</span></span>
<span data-ttu-id="a0f02-122">Указывает имя сервера Microsoft SQL Server, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="a0f02-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="a0f02-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0f02-123">-Confirm</span></span>
<span data-ttu-id="a0f02-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a0f02-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0f02-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0f02-125">-WhatIf</span></span>
<span data-ttu-id="a0f02-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a0f02-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0f02-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a0f02-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0f02-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f02-128">CommonParameters</span></span>
<span data-ttu-id="a0f02-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a0f02-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f02-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0f02-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f02-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a0f02-131">INPUTS</span></span>

### <span data-ttu-id="a0f02-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a0f02-132">System.String</span></span>

### <span data-ttu-id="a0f02-133">System. Nullable "1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a0f02-133">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a0f02-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0f02-134">OUTPUTS</span></span>

### <span data-ttu-id="a0f02-135">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="a0f02-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="a0f02-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="a0f02-136">NOTES</span></span>

## <span data-ttu-id="a0f02-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0f02-137">RELATED LINKS</span></span>
