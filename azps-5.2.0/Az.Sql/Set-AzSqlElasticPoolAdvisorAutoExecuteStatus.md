---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 5e26be318f439556a7083dc4d2bcde154083f5e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395924"
---
# <span data-ttu-id="d549b-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="d549b-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="d549b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d549b-102">SYNOPSIS</span></span>
<span data-ttu-id="d549b-103">Обновляет состояние автоматического выполнения помощника по SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d549b-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="d549b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d549b-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d549b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d549b-105">DESCRIPTION</span></span>
<span data-ttu-id="d549b-106">Cmdlet **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** задает автоматическое выполнение свойства для помощника по SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d549b-106">The **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="d549b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d549b-107">EXAMPLES</span></span>

### <span data-ttu-id="d549b-108">Пример 1. Включить автоматическое выполнение для помощника</span><span class="sxs-lookup"><span data-stu-id="d549b-108">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
'Enabled'ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : ElasticPool
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="d549b-109">Эта команда задает состояние автоматического выполнения помощника CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="d549b-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="d549b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d549b-110">PARAMETERS</span></span>

### <span data-ttu-id="d549b-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="d549b-111">-AdvisorName</span></span>
<span data-ttu-id="d549b-112">Указывает имя помощника, для которого этот cmdlet обновляет состояние автоматического выполнения.</span><span class="sxs-lookup"><span data-stu-id="d549b-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="d549b-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="d549b-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="d549b-114">Указывает новое значение, для которого этот cmdlet обновляет состояние автоматического выполнения.</span><span class="sxs-lookup"><span data-stu-id="d549b-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="d549b-115">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="d549b-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d549b-116">Включено</span><span class="sxs-lookup"><span data-stu-id="d549b-116">Enabled</span></span>
- <span data-ttu-id="d549b-117">Отключено</span><span class="sxs-lookup"><span data-stu-id="d549b-117">Disabled</span></span>
- <span data-ttu-id="d549b-118">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="d549b-118">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d549b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d549b-119">-DefaultProfile</span></span>
<span data-ttu-id="d549b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d549b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d549b-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d549b-121">-ElasticPoolName</span></span>
<span data-ttu-id="d549b-122">Определяет имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="d549b-122">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="d549b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d549b-123">-ResourceGroupName</span></span>
<span data-ttu-id="d549b-124">Указывает имя группы ресурсов сервера, который содержит этот эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="d549b-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="d549b-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d549b-125">-ServerName</span></span>
<span data-ttu-id="d549b-126">Указывает имя сервера, на который находится эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="d549b-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="d549b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d549b-127">-Confirm</span></span>
<span data-ttu-id="d549b-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d549b-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d549b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d549b-129">-WhatIf</span></span>
<span data-ttu-id="d549b-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d549b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d549b-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d549b-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d549b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d549b-132">CommonParameters</span></span>
<span data-ttu-id="d549b-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d549b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d549b-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d549b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d549b-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d549b-135">INPUTS</span></span>

### <span data-ttu-id="d549b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d549b-136">System.String</span></span>

### <span data-ttu-id="d549b-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="d549b-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="d549b-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d549b-138">OUTPUTS</span></span>

### <span data-ttu-id="d549b-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="d549b-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="d549b-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d549b-140">NOTES</span></span>
* <span data-ttu-id="d549b-141">Ключевые слова: azure, azurerm, arm, ресурс, управление, руководитель, sql, эластичный пул, mssql, консультант</span><span class="sxs-lookup"><span data-stu-id="d549b-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="d549b-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d549b-142">RELATED LINKS</span></span>

[<span data-ttu-id="d549b-143">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="d549b-143">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="d549b-144">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="d549b-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
