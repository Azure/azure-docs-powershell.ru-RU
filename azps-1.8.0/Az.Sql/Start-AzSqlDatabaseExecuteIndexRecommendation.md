---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 1ab1e223ec173cf5727011956f52979026159594
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399521"
---
# <span data-ttu-id="eca6e-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="eca6e-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="eca6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eca6e-102">SYNOPSIS</span></span>
<span data-ttu-id="eca6e-103">Запуск рабочего процесса, в который выполняется рекомендуемая операция индексации.</span><span class="sxs-lookup"><span data-stu-id="eca6e-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="eca6e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eca6e-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eca6e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eca6e-105">DESCRIPTION</span></span>
<span data-ttu-id="eca6e-106">Для запуска рабочего процесса, который выполняет рекомендуемую операцию индексирования для базы данных Azure SQL, запускается рабочий процесс **Start-AzSqlDatabaseExecuteIndexRecommendation.**</span><span class="sxs-lookup"><span data-stu-id="eca6e-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="eca6e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eca6e-107">EXAMPLES</span></span>

### <span data-ttu-id="eca6e-108">Пример 1. Запуск рекомендации по индексу</span><span class="sxs-lookup"><span data-stu-id="eca6e-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="eca6e-109">Эта команда выполняет рекомендации по индексу.</span><span class="sxs-lookup"><span data-stu-id="eca6e-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="eca6e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eca6e-110">PARAMETERS</span></span>

### <span data-ttu-id="eca6e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eca6e-111">-DatabaseName</span></span>
<span data-ttu-id="eca6e-112">Указывает имя базы данных, для которой запускается рабочий процесс этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eca6e-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="eca6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eca6e-113">-DefaultProfile</span></span>
<span data-ttu-id="eca6e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eca6e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eca6e-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="eca6e-115">-IndexRecommendationName</span></span>
<span data-ttu-id="eca6e-116">Указывает имя рекомендации по индексу, которую выполняет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eca6e-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="eca6e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eca6e-117">-ResourceGroupName</span></span>
<span data-ttu-id="eca6e-118">Имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="eca6e-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="eca6e-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="eca6e-119">-ServerName</span></span>
<span data-ttu-id="eca6e-120">Сервер, на котором размещена база данных, для которой запускается рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="eca6e-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="eca6e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eca6e-121">CommonParameters</span></span>
<span data-ttu-id="eca6e-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eca6e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eca6e-123">Дополнительные сведения см. [в about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eca6e-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eca6e-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eca6e-124">INPUTS</span></span>

### <span data-ttu-id="eca6e-125">System.String</span><span class="sxs-lookup"><span data-stu-id="eca6e-125">System.String</span></span>

## <span data-ttu-id="eca6e-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eca6e-126">OUTPUTS</span></span>

### <span data-ttu-id="eca6e-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="eca6e-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="eca6e-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eca6e-128">NOTES</span></span>

## <span data-ttu-id="eca6e-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eca6e-129">RELATED LINKS</span></span>


[<span data-ttu-id="eca6e-130">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="eca6e-130">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="eca6e-131">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="eca6e-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


