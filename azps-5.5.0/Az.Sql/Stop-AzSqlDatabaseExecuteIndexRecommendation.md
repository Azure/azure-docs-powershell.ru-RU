---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ca7aeed13627bba3c380b3f1062ee80fcc7c3ebf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241928"
---
# <span data-ttu-id="96499-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="96499-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="96499-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96499-102">SYNOPSIS</span></span>
<span data-ttu-id="96499-103">Остановка рабочего процесса, который выполняет рекомендуемую операцию индексации.</span><span class="sxs-lookup"><span data-stu-id="96499-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="96499-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="96499-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96499-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96499-105">DESCRIPTION</span></span>
<span data-ttu-id="96499-106">Cmdlet **Stop-AzSqlDatabaseExecuteIndexRecommendation** останавливает рабочий процесс, который выполняет рекомендуемую операцию индексирования.</span><span class="sxs-lookup"><span data-stu-id="96499-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="96499-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="96499-107">EXAMPLES</span></span>

### <span data-ttu-id="96499-108">Пример 1. Остановка рекомендации по индексам</span><span class="sxs-lookup"><span data-stu-id="96499-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="96499-109">Эта команда прекращает работу рекомендации по индексу.</span><span class="sxs-lookup"><span data-stu-id="96499-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="96499-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96499-110">PARAMETERS</span></span>

### <span data-ttu-id="96499-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="96499-111">-DatabaseName</span></span>
<span data-ttu-id="96499-112">Имя базы данных, для которой этот cmdlet останавливает рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="96499-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="96499-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96499-113">-DefaultProfile</span></span>
<span data-ttu-id="96499-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="96499-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96499-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="96499-115">-IndexRecommendationName</span></span>
<span data-ttu-id="96499-116">Указывает имя рекомендации по индексу, который останавливает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96499-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="96499-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96499-117">-ResourceGroupName</span></span>
<span data-ttu-id="96499-118">Имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="96499-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="96499-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="96499-119">-ServerName</span></span>
<span data-ttu-id="96499-120">Сервер, на котором размещена база данных, для которой этот cmdlet останавливает рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="96499-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="96499-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96499-121">CommonParameters</span></span>
<span data-ttu-id="96499-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96499-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96499-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96499-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96499-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96499-124">INPUTS</span></span>

### <span data-ttu-id="96499-125">System.String</span><span class="sxs-lookup"><span data-stu-id="96499-125">System.String</span></span>

## <span data-ttu-id="96499-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="96499-126">OUTPUTS</span></span>

### <span data-ttu-id="96499-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="96499-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="96499-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="96499-128">NOTES</span></span>

## <span data-ttu-id="96499-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96499-129">RELATED LINKS</span></span>

[<span data-ttu-id="96499-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="96499-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="96499-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="96499-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="96499-132">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="96499-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


