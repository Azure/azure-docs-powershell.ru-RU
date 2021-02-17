---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 7f13b1a1a5daad4e7c97de962943bb859f6a09df
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399487"
---
# <span data-ttu-id="6cce7-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6cce7-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="6cce7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cce7-102">SYNOPSIS</span></span>
<span data-ttu-id="6cce7-103">Остановка рабочего процесса, который выполняет рекомендуемую операцию индексации.</span><span class="sxs-lookup"><span data-stu-id="6cce7-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="6cce7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6cce7-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cce7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cce7-105">DESCRIPTION</span></span>
<span data-ttu-id="6cce7-106">Cmdlet **Stop-AzSqlDatabaseExecuteIndexRecommendation** останавливает рабочий процесс, который выполняет рекомендуемую операцию индексирования.</span><span class="sxs-lookup"><span data-stu-id="6cce7-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="6cce7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6cce7-107">EXAMPLES</span></span>

### <span data-ttu-id="6cce7-108">Пример 1. Остановка рекомендации по индексам</span><span class="sxs-lookup"><span data-stu-id="6cce7-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="6cce7-109">Эта команда прекращает работу рекомендации по индексу.</span><span class="sxs-lookup"><span data-stu-id="6cce7-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="6cce7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cce7-110">PARAMETERS</span></span>

### <span data-ttu-id="6cce7-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6cce7-111">-DatabaseName</span></span>
<span data-ttu-id="6cce7-112">Имя базы данных, для которой этот cmdlet останавливает рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="6cce7-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="6cce7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cce7-113">-DefaultProfile</span></span>
<span data-ttu-id="6cce7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6cce7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cce7-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="6cce7-115">-IndexRecommendationName</span></span>
<span data-ttu-id="6cce7-116">Указывает имя рекомендации по индексу, который останавливает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cce7-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="6cce7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cce7-117">-ResourceGroupName</span></span>
<span data-ttu-id="6cce7-118">Имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="6cce7-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="6cce7-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6cce7-119">-ServerName</span></span>
<span data-ttu-id="6cce7-120">Сервер, на котором размещена база данных, для которой этот cmdlet останавливает рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="6cce7-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="6cce7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cce7-121">CommonParameters</span></span>
<span data-ttu-id="6cce7-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cce7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cce7-123">Дополнительные сведения см. [в about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cce7-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cce7-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cce7-124">INPUTS</span></span>

### <span data-ttu-id="6cce7-125">System.String</span><span class="sxs-lookup"><span data-stu-id="6cce7-125">System.String</span></span>

## <span data-ttu-id="6cce7-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6cce7-126">OUTPUTS</span></span>

### <span data-ttu-id="6cce7-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6cce7-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="6cce7-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6cce7-128">NOTES</span></span>

## <span data-ttu-id="6cce7-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6cce7-129">RELATED LINKS</span></span>


[<span data-ttu-id="6cce7-130">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6cce7-130">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="6cce7-131">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="6cce7-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


