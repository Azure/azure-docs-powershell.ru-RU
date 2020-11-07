---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
ms.openlocfilehash: f4f3b935aa9303ab38888d6f28f0a89bbdeb6c23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728734"
---
# <span data-ttu-id="23391-101">Stop-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="23391-101">Stop-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="23391-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23391-102">SYNOPSIS</span></span>
<span data-ttu-id="23391-103">Отменяет операцию асинхронных обновлений для базы данных.</span><span class="sxs-lookup"><span data-stu-id="23391-103">Cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="23391-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23391-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23391-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23391-105">DESCRIPTION</span></span>
<span data-ttu-id="23391-106">Командлет **Stop-AzSqlDatabaseActivity** отменяет операцию асинхронных обновлений для базы данных.</span><span class="sxs-lookup"><span data-stu-id="23391-106">The **Stop-AzSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="23391-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23391-107">EXAMPLES</span></span>

### <span data-ttu-id="23391-108">Пример 1: отмена операции асинхронных обновлений для базы данных</span><span class="sxs-lookup"><span data-stu-id="23391-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

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

<span data-ttu-id="23391-109">Эта команда отменяет операцию асинхронных обновлений для базы данных.</span><span class="sxs-lookup"><span data-stu-id="23391-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="23391-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23391-110">PARAMETERS</span></span>

### <span data-ttu-id="23391-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="23391-111">-DatabaseName</span></span>
<span data-ttu-id="23391-112">Указывает имя базы данных, для которой этот командлет получает состояние.</span><span class="sxs-lookup"><span data-stu-id="23391-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="23391-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23391-113">-DefaultProfile</span></span>
<span data-ttu-id="23391-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23391-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23391-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="23391-115">-ElasticPoolName</span></span>
<span data-ttu-id="23391-116">Имя пула эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="23391-116">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="23391-117">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="23391-117">-OperationId</span></span>
<span data-ttu-id="23391-118">Указывает идентификатор операции, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="23391-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="23391-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23391-119">-ResourceGroupName</span></span>
<span data-ttu-id="23391-120">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="23391-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="23391-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="23391-121">-ServerName</span></span>
<span data-ttu-id="23391-122">Указывает имя сервера Microsoft SQL Server, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="23391-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="23391-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23391-123">-Confirm</span></span>
<span data-ttu-id="23391-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="23391-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23391-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23391-125">-WhatIf</span></span>
<span data-ttu-id="23391-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="23391-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23391-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="23391-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23391-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23391-128">CommonParameters</span></span>
<span data-ttu-id="23391-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23391-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23391-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23391-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23391-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23391-131">INPUTS</span></span>

### <span data-ttu-id="23391-132">System. String</span><span class="sxs-lookup"><span data-stu-id="23391-132">System.String</span></span>

### <span data-ttu-id="23391-133">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="23391-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="23391-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23391-134">OUTPUTS</span></span>

### <span data-ttu-id="23391-135">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="23391-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="23391-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="23391-136">NOTES</span></span>

## <span data-ttu-id="23391-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23391-137">RELATED LINKS</span></span>
