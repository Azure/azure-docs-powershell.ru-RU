---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 89b9b5df2f8233254d4c1cb430a80f0a8a91c13b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229676"
---
# <span data-ttu-id="43c9a-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="43c9a-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="43c9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43c9a-102">SYNOPSIS</span></span>
<span data-ttu-id="43c9a-103">Возвращает рекомендуемые типы данных и метки конфиденциальности для столбцов в SQL пуле.</span><span class="sxs-lookup"><span data-stu-id="43c9a-103">Gets the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="43c9a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="43c9a-104">SYNTAX</span></span>

### <span data-ttu-id="43c9a-105">SqlPoolObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="43c9a-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43c9a-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="43c9a-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43c9a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43c9a-107">DESCRIPTION</span></span>
<span data-ttu-id="43c9a-108">Этот Get-AzSynapseSqlPoolSensitivityRecommendation возвращает рекомендуемые типы информации и метки конфиденциальности столбцов в SQL пуле.</span><span class="sxs-lookup"><span data-stu-id="43c9a-108">The Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="43c9a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="43c9a-109">EXAMPLES</span></span>

### <span data-ttu-id="43c9a-110">Пример 1. Получите рекомендуемые типы данных и метки конфиденциальности для пула Azure Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="43c9a-110">Example 1: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="43c9a-111">Пример 2. Получите рекомендуемые типы данных и метки конфиденциальности для пула Azure Synapse SQL с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="43c9a-111">Example 2: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityRecommendation

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="43c9a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43c9a-112">PARAMETERS</span></span>

### <span data-ttu-id="43c9a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43c9a-113">-AsJob</span></span>
<span data-ttu-id="43c9a-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="43c9a-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c9a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43c9a-115">-DefaultProfile</span></span>
<span data-ttu-id="43c9a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43c9a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43c9a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43c9a-117">-ResourceGroupName</span></span>
<span data-ttu-id="43c9a-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="43c9a-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c9a-119">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="43c9a-119">-SqlPoolName</span></span>
<span data-ttu-id="43c9a-120">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="43c9a-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c9a-121">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="43c9a-121">-SqlPoolObject</span></span>
<span data-ttu-id="43c9a-122">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="43c9a-122">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43c9a-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="43c9a-123">-WorkspaceName</span></span>
<span data-ttu-id="43c9a-124">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="43c9a-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c9a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c9a-125">CommonParameters</span></span>
<span data-ttu-id="43c9a-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43c9a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c9a-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43c9a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c9a-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43c9a-128">INPUTS</span></span>

### <span data-ttu-id="43c9a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="43c9a-129">System.String</span></span>

### <span data-ttu-id="43c9a-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="43c9a-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="43c9a-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="43c9a-131">OUTPUTS</span></span>

### <span data-ttu-id="43c9a-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="43c9a-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="43c9a-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="43c9a-133">NOTES</span></span>

## <span data-ttu-id="43c9a-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43c9a-134">RELATED LINKS</span></span>
