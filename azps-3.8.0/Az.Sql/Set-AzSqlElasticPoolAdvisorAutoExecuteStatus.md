---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 5e26be318f439556a7083dc4d2bcde154083f5e4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912597"
---
# <span data-ttu-id="3a661-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="3a661-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="3a661-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a661-102">SYNOPSIS</span></span>
<span data-ttu-id="3a661-103">Обновляет состояние автоматического выполнения советника по пулам эластичных БД Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="3a661-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="3a661-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a661-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a661-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a661-105">DESCRIPTION</span></span>
<span data-ttu-id="3a661-106">Командлет **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** задает свойство автоматического выполнения для помощника по пулам эластичных БД Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="3a661-106">The **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="3a661-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a661-107">EXAMPLES</span></span>

### <span data-ttu-id="3a661-108">Пример 1: Включение автоматического выполнения для помощника</span><span class="sxs-lookup"><span data-stu-id="3a661-108">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="3a661-109">Эта команда устанавливает состояние автоматического выполнения для помощника с именем CreateIndex на Enabled.</span><span class="sxs-lookup"><span data-stu-id="3a661-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="3a661-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a661-110">PARAMETERS</span></span>

### <span data-ttu-id="3a661-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="3a661-111">-AdvisorName</span></span>
<span data-ttu-id="3a661-112">Указывает имя помощника, для которого этот командлет обновляет состояние автоматического выполнения.</span><span class="sxs-lookup"><span data-stu-id="3a661-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="3a661-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="3a661-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="3a661-114">Указывает новое значение, на которое этот командлет обновляет состояние автоматического выполнения.</span><span class="sxs-lookup"><span data-stu-id="3a661-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="3a661-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3a661-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3a661-116">Включаем</span><span class="sxs-lookup"><span data-stu-id="3a661-116">Enabled</span></span>
- <span data-ttu-id="3a661-117">Отключает</span><span class="sxs-lookup"><span data-stu-id="3a661-117">Disabled</span></span>
- <span data-ttu-id="3a661-118">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="3a661-118">Default</span></span>

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

### <span data-ttu-id="3a661-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a661-119">-DefaultProfile</span></span>
<span data-ttu-id="3a661-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3a661-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a661-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3a661-121">-ElasticPoolName</span></span>
<span data-ttu-id="3a661-122">Указывает имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="3a661-122">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="3a661-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a661-123">-ResourceGroupName</span></span>
<span data-ttu-id="3a661-124">Указывает имя группы ресурсов сервера, содержащего этот эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="3a661-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="3a661-125">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="3a661-125">-ServerName</span></span>
<span data-ttu-id="3a661-126">Указывает имя сервера, на котором находится пул эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="3a661-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="3a661-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a661-127">-Confirm</span></span>
<span data-ttu-id="3a661-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3a661-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a661-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a661-129">-WhatIf</span></span>
<span data-ttu-id="3a661-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3a661-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a661-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3a661-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a661-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a661-132">CommonParameters</span></span>
<span data-ttu-id="3a661-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a661-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a661-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a661-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a661-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a661-135">INPUTS</span></span>

### <span data-ttu-id="3a661-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3a661-136">System.String</span></span>

### <span data-ttu-id="3a661-137">Microsoft. Azure. Commands. SQL. Advisor. командлет. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="3a661-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="3a661-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a661-138">OUTPUTS</span></span>

### <span data-ttu-id="3a661-139">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="3a661-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="3a661-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a661-140">NOTES</span></span>
* <span data-ttu-id="3a661-141">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, эластичный пул, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="3a661-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="3a661-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a661-142">RELATED LINKS</span></span>

[<span data-ttu-id="3a661-143">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="3a661-143">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="3a661-144">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="3a661-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
