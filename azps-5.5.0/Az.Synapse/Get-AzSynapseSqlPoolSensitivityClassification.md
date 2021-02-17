---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 6affe94fdbfa7a698ad7d666d1847365fc8e25ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231433"
---
# <span data-ttu-id="f3679-101">Get-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="f3679-101">Get-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="f3679-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3679-102">SYNOPSIS</span></span>
<span data-ttu-id="f3679-103">Возвращает текущие типы данных и метки конфиденциальности столбцов в SQL пуле.</span><span class="sxs-lookup"><span data-stu-id="f3679-103">Gets the current information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="f3679-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f3679-104">SYNTAX</span></span>

### <span data-ttu-id="f3679-105">SqlPoolObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f3679-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3679-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3679-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3679-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3679-107">ColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3679-108">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3679-108">SqlPoolObjectColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3679-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3679-109">DESCRIPTION</span></span>
<span data-ttu-id="f3679-110">Этот Get-AzSynapseSqlPoolSensitivityClassification возвращает текущие типы данных и метки конфиденциальности столбцов в SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="f3679-110">The Get-AzSynapseSqlPoolSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure Synapse SQL pool.</span></span>

## <span data-ttu-id="f3679-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f3679-111">EXAMPLES</span></span>

### <span data-ttu-id="f3679-112">Пример 1. Получите текущие типы данных и метки конфиденциальности для пула Azure Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="f3679-112">Example 1: Get current information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool

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

### <span data-ttu-id="f3679-113">Пример 2. Получите текущие типы данных и метки конфиденциальности пула Azure Synapse SQL Piping.</span><span class="sxs-lookup"><span data-stu-id="f3679-113">Example 2: Get current information types and sensitivity labels of an Azure Synapse SQL pool with Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityClassification

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

### <span data-ttu-id="f3679-114">Пример 3. Получите текущий тип данных и метку конфиденциальности для определенного столбца в SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="f3679-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="f3679-115">Пример 4. Получите текущий тип данных и метку конфиденциальности для определенного столбца в SQL Azure Synapse с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="f3679-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="f3679-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3679-116">PARAMETERS</span></span>

### <span data-ttu-id="f3679-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3679-117">-AsJob</span></span>
<span data-ttu-id="f3679-118">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f3679-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3679-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="f3679-119">-ColumnName</span></span>
<span data-ttu-id="f3679-120">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="f3679-120">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3679-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3679-121">-DefaultProfile</span></span>
<span data-ttu-id="f3679-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3679-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3679-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3679-123">-ResourceGroupName</span></span>
<span data-ttu-id="f3679-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f3679-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3679-125">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="f3679-125">-SchemaName</span></span>
<span data-ttu-id="f3679-126">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="f3679-126">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3679-127">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="f3679-127">-SqlPoolName</span></span>
<span data-ttu-id="f3679-128">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="f3679-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3679-129">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="f3679-129">-SqlPoolObject</span></span>
<span data-ttu-id="f3679-130">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="f3679-130">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3679-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="f3679-131">-TableName</span></span>
<span data-ttu-id="f3679-132">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="f3679-132">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3679-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f3679-133">-WorkspaceName</span></span>
<span data-ttu-id="f3679-134">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="f3679-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3679-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3679-135">CommonParameters</span></span>
<span data-ttu-id="f3679-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3679-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3679-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3679-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3679-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3679-138">INPUTS</span></span>

### <span data-ttu-id="f3679-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f3679-139">System.String</span></span>

### <span data-ttu-id="f3679-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f3679-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="f3679-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f3679-141">OUTPUTS</span></span>

### <span data-ttu-id="f3679-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="f3679-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="f3679-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f3679-143">NOTES</span></span>

## <span data-ttu-id="f3679-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3679-144">RELATED LINKS</span></span>
