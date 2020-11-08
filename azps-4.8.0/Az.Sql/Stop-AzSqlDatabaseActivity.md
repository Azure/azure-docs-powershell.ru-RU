---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
ms.openlocfilehash: f6beaa0651e406d94e1718bb1b1fdea6ef1c3507
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077549"
---
# <span data-ttu-id="2f021-101">Stop-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="2f021-101">Stop-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="2f021-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f021-102">SYNOPSIS</span></span>
<span data-ttu-id="2f021-103">Отменяет операцию асинхронных обновлений для базы данных.</span><span class="sxs-lookup"><span data-stu-id="2f021-103">Cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="2f021-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f021-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f021-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f021-105">DESCRIPTION</span></span>
<span data-ttu-id="2f021-106">Командлет **Stop-AzSqlDatabaseActivity** отменяет операцию асинхронных обновлений для базы данных.</span><span class="sxs-lookup"><span data-stu-id="2f021-106">The **Stop-AzSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="2f021-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f021-107">EXAMPLES</span></span>

### <span data-ttu-id="2f021-108">Пример 1: отмена операции асинхронных обновлений для базы данных</span><span class="sxs-lookup"><span data-stu-id="2f021-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
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

<span data-ttu-id="2f021-109">Эта команда отменяет операцию асинхронных обновлений для базы данных.</span><span class="sxs-lookup"><span data-stu-id="2f021-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="2f021-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f021-110">PARAMETERS</span></span>

### <span data-ttu-id="2f021-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2f021-111">-DatabaseName</span></span>
<span data-ttu-id="2f021-112">Указывает имя базы данных, для которой этот командлет получает состояние.</span><span class="sxs-lookup"><span data-stu-id="2f021-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="2f021-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f021-113">-DefaultProfile</span></span>
<span data-ttu-id="2f021-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f021-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f021-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="2f021-115">-ElasticPoolName</span></span>
<span data-ttu-id="2f021-116">Имя пула эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2f021-116">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="2f021-117">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="2f021-117">-OperationId</span></span>
<span data-ttu-id="2f021-118">Указывает идентификатор операции, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2f021-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2f021-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f021-119">-ResourceGroupName</span></span>
<span data-ttu-id="2f021-120">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="2f021-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="2f021-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="2f021-121">-ServerName</span></span>
<span data-ttu-id="2f021-122">Указывает имя сервера Microsoft SQL Server, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="2f021-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="2f021-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f021-123">-Confirm</span></span>
<span data-ttu-id="2f021-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2f021-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f021-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f021-125">-WhatIf</span></span>
<span data-ttu-id="2f021-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2f021-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f021-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2f021-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f021-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f021-128">CommonParameters</span></span>
<span data-ttu-id="2f021-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f021-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f021-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f021-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f021-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f021-131">INPUTS</span></span>

### <span data-ttu-id="2f021-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2f021-132">System.String</span></span>

### <span data-ttu-id="2f021-133">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2f021-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2f021-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f021-134">OUTPUTS</span></span>

### <span data-ttu-id="2f021-135">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="2f021-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="2f021-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f021-136">NOTES</span></span>

## <span data-ttu-id="2f021-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f021-137">RELATED LINKS</span></span>
