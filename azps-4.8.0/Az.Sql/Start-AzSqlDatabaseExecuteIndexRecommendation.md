---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: e69cffe6955a5bf19636dd519c0906be64ce4413
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243847"
---
# <span data-ttu-id="879e2-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="879e2-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="879e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="879e2-102">SYNOPSIS</span></span>
<span data-ttu-id="879e2-103">Запускает рабочий процесс, который запускает рекомендованную операцию с индексами.</span><span class="sxs-lookup"><span data-stu-id="879e2-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="879e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="879e2-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="879e2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="879e2-105">DESCRIPTION</span></span>
<span data-ttu-id="879e2-106">Командлет **Start-AzSqlDatabaseExecuteIndexRecommendation** запускает рабочий процесс, который запускает рекомендованную операцию с индексами для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="879e2-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="879e2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="879e2-107">EXAMPLES</span></span>

### <span data-ttu-id="879e2-108">Пример 1: выполнение рекомендации по индексу</span><span class="sxs-lookup"><span data-stu-id="879e2-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="879e2-109">Эта команда запускает рекомендации по индексу.</span><span class="sxs-lookup"><span data-stu-id="879e2-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="879e2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="879e2-110">PARAMETERS</span></span>

### <span data-ttu-id="879e2-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="879e2-111">-DatabaseName</span></span>
<span data-ttu-id="879e2-112">Указывает имя базы данных, для которой этот командлет запускает рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="879e2-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="879e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="879e2-113">-DefaultProfile</span></span>
<span data-ttu-id="879e2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="879e2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="879e2-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="879e2-115">-IndexRecommendationName</span></span>
<span data-ttu-id="879e2-116">Указывает имя рекомендации по индексированию, которое будет запущено этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="879e2-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="879e2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="879e2-117">-ResourceGroupName</span></span>
<span data-ttu-id="879e2-118">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="879e2-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="879e2-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="879e2-119">-ServerName</span></span>
<span data-ttu-id="879e2-120">Указывает сервер, на котором размещена база данных, для которой этот командлет запускает рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="879e2-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="879e2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="879e2-121">CommonParameters</span></span>
<span data-ttu-id="879e2-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="879e2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="879e2-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="879e2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="879e2-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="879e2-124">INPUTS</span></span>

### <span data-ttu-id="879e2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="879e2-125">System.String</span></span>

## <span data-ttu-id="879e2-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="879e2-126">OUTPUTS</span></span>

### <span data-ttu-id="879e2-127">Microsoft. Azure. Commands. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="879e2-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="879e2-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="879e2-128">NOTES</span></span>

## <span data-ttu-id="879e2-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="879e2-129">RELATED LINKS</span></span>

[<span data-ttu-id="879e2-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="879e2-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="879e2-131">Остановить-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="879e2-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="879e2-132">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="879e2-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

