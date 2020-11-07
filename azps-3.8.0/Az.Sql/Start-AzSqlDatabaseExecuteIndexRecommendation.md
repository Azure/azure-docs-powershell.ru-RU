---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: e69cffe6955a5bf19636dd519c0906be64ce4413
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912489"
---
# <span data-ttu-id="5ee43-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="5ee43-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="5ee43-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ee43-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee43-103">Запускает рабочий процесс, который запускает рекомендованную операцию с индексами.</span><span class="sxs-lookup"><span data-stu-id="5ee43-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="5ee43-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ee43-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ee43-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ee43-105">DESCRIPTION</span></span>
<span data-ttu-id="5ee43-106">Командлет **Start-AzSqlDatabaseExecuteIndexRecommendation** запускает рабочий процесс, который запускает рекомендованную операцию с индексами для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5ee43-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="5ee43-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ee43-107">EXAMPLES</span></span>

### <span data-ttu-id="5ee43-108">Пример 1: выполнение рекомендации по индексу</span><span class="sxs-lookup"><span data-stu-id="5ee43-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="5ee43-109">Эта команда запускает рекомендации по индексу.</span><span class="sxs-lookup"><span data-stu-id="5ee43-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="5ee43-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ee43-110">PARAMETERS</span></span>

### <span data-ttu-id="5ee43-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5ee43-111">-DatabaseName</span></span>
<span data-ttu-id="5ee43-112">Указывает имя базы данных, для которой этот командлет запускает рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="5ee43-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="5ee43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee43-113">-DefaultProfile</span></span>
<span data-ttu-id="5ee43-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5ee43-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ee43-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="5ee43-115">-IndexRecommendationName</span></span>
<span data-ttu-id="5ee43-116">Указывает имя рекомендации по индексированию, которое будет запущено этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5ee43-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="5ee43-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ee43-117">-ResourceGroupName</span></span>
<span data-ttu-id="5ee43-118">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="5ee43-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5ee43-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="5ee43-119">-ServerName</span></span>
<span data-ttu-id="5ee43-120">Указывает сервер, на котором размещена база данных, для которой этот командлет запускает рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="5ee43-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="5ee43-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee43-121">CommonParameters</span></span>
<span data-ttu-id="5ee43-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ee43-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee43-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ee43-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee43-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ee43-124">INPUTS</span></span>

### <span data-ttu-id="5ee43-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5ee43-125">System.String</span></span>

## <span data-ttu-id="5ee43-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ee43-126">OUTPUTS</span></span>

### <span data-ttu-id="5ee43-127">Microsoft. Azure. Commands. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="5ee43-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="5ee43-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ee43-128">NOTES</span></span>

## <span data-ttu-id="5ee43-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ee43-129">RELATED LINKS</span></span>

[<span data-ttu-id="5ee43-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="5ee43-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="5ee43-131">Остановить-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="5ee43-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="5ee43-132">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="5ee43-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


