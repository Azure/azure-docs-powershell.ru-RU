---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ca7aeed13627bba3c380b3f1062ee80fcc7c3ebf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077548"
---
# <span data-ttu-id="6fdaf-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6fdaf-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="6fdaf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6fdaf-102">SYNOPSIS</span></span>
<span data-ttu-id="6fdaf-103">Останавливает рабочий процесс, который запускает рекомендованную операцию с индексами.</span><span class="sxs-lookup"><span data-stu-id="6fdaf-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="6fdaf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6fdaf-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6fdaf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fdaf-105">DESCRIPTION</span></span>
<span data-ttu-id="6fdaf-106">Командлет **Stop-AzSqlDatabaseExecuteIndexRecommendation** останавливает рабочий процесс, который запускает рекомендованную операцию с индексами.</span><span class="sxs-lookup"><span data-stu-id="6fdaf-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="6fdaf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6fdaf-107">EXAMPLES</span></span>

### <span data-ttu-id="6fdaf-108">Пример 1: остановка выполнения рекомендации по индексу</span><span class="sxs-lookup"><span data-stu-id="6fdaf-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="6fdaf-109">Эта команда прекращает выполнение рекомендации по индексу.</span><span class="sxs-lookup"><span data-stu-id="6fdaf-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="6fdaf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6fdaf-110">PARAMETERS</span></span>

### <span data-ttu-id="6fdaf-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6fdaf-111">-DatabaseName</span></span>
<span data-ttu-id="6fdaf-112">Указывает имя базы данных, для которой этот командлет останавливает рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="6fdaf-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="6fdaf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fdaf-113">-DefaultProfile</span></span>
<span data-ttu-id="6fdaf-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6fdaf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6fdaf-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="6fdaf-115">-IndexRecommendationName</span></span>
<span data-ttu-id="6fdaf-116">Указывает имя рекомендации по индексированию, которое прерывается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6fdaf-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="6fdaf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fdaf-117">-ResourceGroupName</span></span>
<span data-ttu-id="6fdaf-118">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="6fdaf-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="6fdaf-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="6fdaf-119">-ServerName</span></span>
<span data-ttu-id="6fdaf-120">Указывает сервер, на котором размещается база данных, для которой этот командлет останавливает рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="6fdaf-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="6fdaf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fdaf-121">CommonParameters</span></span>
<span data-ttu-id="6fdaf-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6fdaf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fdaf-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fdaf-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fdaf-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6fdaf-124">INPUTS</span></span>

### <span data-ttu-id="6fdaf-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6fdaf-125">System.String</span></span>

## <span data-ttu-id="6fdaf-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fdaf-126">OUTPUTS</span></span>

### <span data-ttu-id="6fdaf-127">Microsoft. Azure. Commands. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6fdaf-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="6fdaf-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="6fdaf-128">NOTES</span></span>

## <span data-ttu-id="6fdaf-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6fdaf-129">RELATED LINKS</span></span>

[<span data-ttu-id="6fdaf-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6fdaf-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="6fdaf-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6fdaf-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="6fdaf-132">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="6fdaf-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

