---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: cf9250080e0d8e079257a4996b7d263bd96a2093
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078676"
---
# <span data-ttu-id="31094-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="31094-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="31094-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31094-102">SYNOPSIS</span></span>
<span data-ttu-id="31094-103">Получает Рекомендуемые типы сведений и метки чувствительности столбцов в базе данных экземпляра SQL, управляемой с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="31094-103">Gets the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="31094-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31094-104">SYNTAX</span></span>

### <span data-ttu-id="31094-105">DatabaseObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31094-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31094-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="31094-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31094-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31094-107">DESCRIPTION</span></span>
<span data-ttu-id="31094-108">Командлет Get-AzSqlInstanceDatabaseSensitivityRecommendation возвращает Рекомендуемые типы данных и метки чувствительности для столбцов в базе данных SQL, управляемой с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="31094-108">The Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="31094-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31094-109">EXAMPLES</span></span>

### <span data-ttu-id="31094-110">Пример 1: получение рекомендуемых типов сведений и меток чувствительности для базы данных экземпляра SQL с управляемой службой Azure.</span><span class="sxs-lookup"><span data-stu-id="31094-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
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

### <span data-ttu-id="31094-111">Пример 2: получение рекомендуемых типов данных и меток чувствительности для базы данных экземпляра SQL с управляемой службой Azure с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="31094-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
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

## <span data-ttu-id="31094-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31094-112">PARAMETERS</span></span>

### <span data-ttu-id="31094-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31094-113">-AsJob</span></span>
<span data-ttu-id="31094-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="31094-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31094-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="31094-115">-DatabaseName</span></span>
<span data-ttu-id="31094-116">Имя базы данных экземпляра SQL, управляемой с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="31094-116">The name of the Azure SQL managed instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31094-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="31094-117">-DatabaseObject</span></span>
<span data-ttu-id="31094-118">Объект базы данных экземпляра SQL, управляемый с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="31094-118">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31094-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31094-119">-DefaultProfile</span></span>
<span data-ttu-id="31094-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31094-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31094-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="31094-121">-InstanceName</span></span>
<span data-ttu-id="31094-122">Имя экземпляра с управляемым SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="31094-122">Azure SQL managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31094-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31094-123">-ResourceGroupName</span></span>
<span data-ttu-id="31094-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31094-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31094-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31094-125">CommonParameters</span></span>
<span data-ttu-id="31094-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31094-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31094-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31094-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31094-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31094-128">INPUTS</span></span>

### <span data-ttu-id="31094-129">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="31094-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="31094-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31094-130">OUTPUTS</span></span>

### <span data-ttu-id="31094-131">Microsoft. Azure. Commands. SQL. Classification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="31094-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="31094-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="31094-132">NOTES</span></span>

## <span data-ttu-id="31094-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31094-133">RELATED LINKS</span></span>

[<span data-ttu-id="31094-134">Дополнительные сведения об обнаружении и классификации данных в базе данных Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="31094-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
