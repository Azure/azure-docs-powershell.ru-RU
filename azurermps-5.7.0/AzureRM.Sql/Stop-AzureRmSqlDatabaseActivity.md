---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: d0aa42b8b584ade698c3d03848a537350ac342d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733208"
---
# <span data-ttu-id="79e96-101">Stop-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="79e96-101">Stop-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="79e96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79e96-102">SYNOPSIS</span></span>
<span data-ttu-id="79e96-103">Отменяет операцию асинхронных обновлений для базы данных.</span><span class="sxs-lookup"><span data-stu-id="79e96-103">Cancels the asynchronous updates operation on the database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79e96-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79e96-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79e96-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79e96-105">DESCRIPTION</span></span>
<span data-ttu-id="79e96-106">Командлет **Stop-AzureRmSqlDatabaseActivity** отменяет операцию асинхронных обновлений для базы данных.</span><span class="sxs-lookup"><span data-stu-id="79e96-106">The **Stop-AzureRmSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="79e96-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79e96-107">EXAMPLES</span></span>

### <span data-ttu-id="79e96-108">Пример 1: отмена операции асинхронных обновлений для базы данных</span><span class="sxs-lookup"><span data-stu-id="79e96-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
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

<span data-ttu-id="79e96-109">Эта команда отменяет операцию асинхронных обновлений для базы данных.</span><span class="sxs-lookup"><span data-stu-id="79e96-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="79e96-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79e96-110">PARAMETERS</span></span>

### <span data-ttu-id="79e96-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="79e96-111">-DatabaseName</span></span>
<span data-ttu-id="79e96-112">Указывает имя базы данных, для которой этот командлет получает состояние.</span><span class="sxs-lookup"><span data-stu-id="79e96-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79e96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79e96-113">-DefaultProfile</span></span>
<span data-ttu-id="79e96-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79e96-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79e96-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="79e96-115">-ElasticPoolName</span></span>
<span data-ttu-id="79e96-116">Имя пула эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="79e96-116">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79e96-117">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="79e96-117">-OperationId</span></span>
<span data-ttu-id="79e96-118">Указывает идентификатор операции, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="79e96-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79e96-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79e96-119">-ResourceGroupName</span></span>
<span data-ttu-id="79e96-120">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="79e96-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="79e96-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="79e96-121">-ServerName</span></span>
<span data-ttu-id="79e96-122">Указывает имя сервера Microsoft SQL Server, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="79e96-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="79e96-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79e96-123">-Confirm</span></span>
<span data-ttu-id="79e96-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="79e96-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79e96-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79e96-125">-WhatIf</span></span>
<span data-ttu-id="79e96-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="79e96-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79e96-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="79e96-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79e96-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79e96-128">CommonParameters</span></span>
<span data-ttu-id="79e96-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79e96-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79e96-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79e96-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79e96-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79e96-131">INPUTS</span></span>

### <span data-ttu-id="79e96-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="79e96-132">None</span></span>
<span data-ttu-id="79e96-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="79e96-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="79e96-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79e96-134">OUTPUTS</span></span>

### <span data-ttu-id="79e96-135">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="79e96-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="79e96-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="79e96-136">NOTES</span></span>

## <span data-ttu-id="79e96-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79e96-137">RELATED LINKS</span></span>
