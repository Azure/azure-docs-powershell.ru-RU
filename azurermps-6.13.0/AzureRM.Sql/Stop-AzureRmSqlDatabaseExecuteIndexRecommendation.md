---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 2922edf4f7b7cfd0d814a5559bb1e6e7bb9ef3ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562519"
---
# <span data-ttu-id="ec97f-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ec97f-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="ec97f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ec97f-102">SYNOPSIS</span></span>
<span data-ttu-id="ec97f-103">Останавливает рабочий процесс, который запускает рекомендованную операцию с индексами.</span><span class="sxs-lookup"><span data-stu-id="ec97f-103">Stops the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec97f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ec97f-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec97f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec97f-105">DESCRIPTION</span></span>
<span data-ttu-id="ec97f-106">Командлет **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** останавливает рабочий процесс, который запускает рекомендованную операцию с индексами.</span><span class="sxs-lookup"><span data-stu-id="ec97f-106">The **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="ec97f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ec97f-107">EXAMPLES</span></span>

### <span data-ttu-id="ec97f-108">Пример 1: остановка выполнения рекомендации по индексу</span><span class="sxs-lookup"><span data-stu-id="ec97f-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="ec97f-109">Эта команда прекращает выполнение рекомендации по индексу.</span><span class="sxs-lookup"><span data-stu-id="ec97f-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="ec97f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ec97f-110">PARAMETERS</span></span>

### <span data-ttu-id="ec97f-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ec97f-111">-DatabaseName</span></span>
<span data-ttu-id="ec97f-112">Указывает имя базы данных, для которой этот командлет останавливает рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="ec97f-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="ec97f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec97f-113">-DefaultProfile</span></span>
<span data-ttu-id="ec97f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ec97f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec97f-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="ec97f-115">-IndexRecommendationName</span></span>
<span data-ttu-id="ec97f-116">Указывает имя рекомендации по индексированию, которое прерывается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ec97f-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="ec97f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec97f-117">-ResourceGroupName</span></span>
<span data-ttu-id="ec97f-118">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="ec97f-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ec97f-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ec97f-119">-ServerName</span></span>
<span data-ttu-id="ec97f-120">Указывает сервер, на котором размещается база данных, для которой этот командлет останавливает рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="ec97f-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="ec97f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec97f-121">CommonParameters</span></span>
<span data-ttu-id="ec97f-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ec97f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec97f-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec97f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec97f-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ec97f-124">INPUTS</span></span>

### <span data-ttu-id="ec97f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ec97f-125">System.String</span></span>

## <span data-ttu-id="ec97f-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec97f-126">OUTPUTS</span></span>

### <span data-ttu-id="ec97f-127">Microsoft. Azure. Commands. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ec97f-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="ec97f-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="ec97f-128">NOTES</span></span>

## <span data-ttu-id="ec97f-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec97f-129">RELATED LINKS</span></span>

[<span data-ttu-id="ec97f-130">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="ec97f-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="ec97f-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ec97f-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="ec97f-132">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="ec97f-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


