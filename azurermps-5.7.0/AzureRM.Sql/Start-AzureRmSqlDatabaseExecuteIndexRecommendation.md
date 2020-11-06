---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ac5bf33bd87ff290784728fd0c4857d5278d3057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566048"
---
# <span data-ttu-id="6f2de-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6f2de-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="6f2de-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f2de-102">SYNOPSIS</span></span>
<span data-ttu-id="6f2de-103">Запускает рабочий процесс, который запускает рекомендованную операцию с индексами.</span><span class="sxs-lookup"><span data-stu-id="6f2de-103">Starts the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f2de-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f2de-104">SYNTAX</span></span>

```
Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f2de-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f2de-105">DESCRIPTION</span></span>
<span data-ttu-id="6f2de-106">Командлет **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** запускает рабочий процесс, который запускает рекомендованную операцию с индексами для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6f2de-106">The **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="6f2de-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f2de-107">EXAMPLES</span></span>

### <span data-ttu-id="6f2de-108">Пример 1: выполнение рекомендации по индексу</span><span class="sxs-lookup"><span data-stu-id="6f2de-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="6f2de-109">Эта команда запускает рекомендации по индексу.</span><span class="sxs-lookup"><span data-stu-id="6f2de-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="6f2de-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f2de-110">PARAMETERS</span></span>

### <span data-ttu-id="6f2de-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6f2de-111">-DatabaseName</span></span>
<span data-ttu-id="6f2de-112">Указывает имя базы данных, для которой этот командлет запускает рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="6f2de-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="6f2de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f2de-113">-DefaultProfile</span></span>
<span data-ttu-id="6f2de-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6f2de-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f2de-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="6f2de-115">-IndexRecommendationName</span></span>
<span data-ttu-id="6f2de-116">Указывает имя рекомендации по индексированию, которое будет запущено этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6f2de-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="6f2de-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f2de-117">-ResourceGroupName</span></span>
<span data-ttu-id="6f2de-118">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="6f2de-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="6f2de-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="6f2de-119">-ServerName</span></span>
<span data-ttu-id="6f2de-120">Указывает сервер, на котором размещена база данных, для которой этот командлет запускает рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="6f2de-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="6f2de-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f2de-121">CommonParameters</span></span>
<span data-ttu-id="6f2de-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f2de-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f2de-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f2de-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f2de-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f2de-124">INPUTS</span></span>

### <span data-ttu-id="6f2de-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="6f2de-125">None</span></span>
<span data-ttu-id="6f2de-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="6f2de-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f2de-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f2de-127">OUTPUTS</span></span>

## <span data-ttu-id="6f2de-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f2de-128">NOTES</span></span>

## <span data-ttu-id="6f2de-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f2de-129">RELATED LINKS</span></span>

[<span data-ttu-id="6f2de-130">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="6f2de-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="6f2de-131">Остановить-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6f2de-131">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="6f2de-132">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="6f2de-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


