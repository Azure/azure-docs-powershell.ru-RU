---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: d2949bf2d366dc64b0e55b82d0c90979042ea294
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985505"
---
# <span data-ttu-id="e9ce2-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="e9ce2-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="e9ce2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9ce2-102">SYNOPSIS</span></span>
<span data-ttu-id="e9ce2-103">Возвращает рекомендуемые типы данных и метки конфиденциальности для столбцов в SQL пуле.</span><span class="sxs-lookup"><span data-stu-id="e9ce2-103">Gets the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="e9ce2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e9ce2-104">SYNTAX</span></span>

### <span data-ttu-id="e9ce2-105">SqlPoolObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e9ce2-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9ce2-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9ce2-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9ce2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9ce2-107">DESCRIPTION</span></span>
<span data-ttu-id="e9ce2-108">Этот Get-AzSynapseSqlPoolSensitivityRecommendation возвращает рекомендуемые типы данных и метки конфиденциальности столбцов в SQL пуле.</span><span class="sxs-lookup"><span data-stu-id="e9ce2-108">The Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="e9ce2-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e9ce2-109">EXAMPLES</span></span>

### <span data-ttu-id="e9ce2-110">Пример 1. Получите рекомендуемые типы данных и метки конфиденциальности для пула Azure Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="e9ce2-110">Example 1: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="e9ce2-111">Пример 2. Получите рекомендуемые типы данных и метки конфиденциальности для пула Azure Synapse SQL с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="e9ce2-111">Example 2: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool using Piping.</span></span>
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

## <span data-ttu-id="e9ce2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9ce2-112">PARAMETERS</span></span>

### <span data-ttu-id="e9ce2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9ce2-113">-AsJob</span></span>
<span data-ttu-id="e9ce2-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e9ce2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9ce2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9ce2-115">-DefaultProfile</span></span>
<span data-ttu-id="e9ce2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9ce2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9ce2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9ce2-117">-ResourceGroupName</span></span>
<span data-ttu-id="e9ce2-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e9ce2-118">Resource group name.</span></span>

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

### <span data-ttu-id="e9ce2-119">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="e9ce2-119">-SqlPoolName</span></span>
<span data-ttu-id="e9ce2-120">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="e9ce2-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="e9ce2-121">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="e9ce2-121">-SqlPoolObject</span></span>
<span data-ttu-id="e9ce2-122">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="e9ce2-122">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e9ce2-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e9ce2-123">-WorkspaceName</span></span>
<span data-ttu-id="e9ce2-124">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="e9ce2-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e9ce2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9ce2-125">CommonParameters</span></span>
<span data-ttu-id="e9ce2-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9ce2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9ce2-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9ce2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9ce2-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9ce2-128">INPUTS</span></span>

### <span data-ttu-id="e9ce2-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e9ce2-129">System.String</span></span>

### <span data-ttu-id="e9ce2-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e9ce2-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e9ce2-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e9ce2-131">OUTPUTS</span></span>

### <span data-ttu-id="e9ce2-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="e9ce2-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="e9ce2-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e9ce2-133">NOTES</span></span>

## <span data-ttu-id="e9ce2-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9ce2-134">RELATED LINKS</span></span>
