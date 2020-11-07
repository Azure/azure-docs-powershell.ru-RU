---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 7af5736e2f66b8bf428815456ba95b3c5b4b6182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732342"
---
# <span data-ttu-id="f22a6-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f22a6-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="f22a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f22a6-102">SYNOPSIS</span></span>
<span data-ttu-id="f22a6-103">Изменяет состояние автоматического выполнения помощника по базам данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f22a6-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f22a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f22a6-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -DatabaseName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f22a6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f22a6-105">DESCRIPTION</span></span>
<span data-ttu-id="f22a6-106">Командлет **Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** изменяет свойство автоматического выполнения для помощника по базам данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f22a6-106">The **Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="f22a6-107">В настоящее время этот командлет поддерживает значения Enabled, Disabled и Default.</span><span class="sxs-lookup"><span data-stu-id="f22a6-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="f22a6-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f22a6-108">EXAMPLES</span></span>

### <span data-ttu-id="f22a6-109">Пример 1: Включение автоматического выполнения для помощника</span><span class="sxs-lookup"><span data-stu-id="f22a6-109">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -ResourceGroupName "ContosoRunnersProd" -ServerName "runner-australia-east" -DatabaseName "ContosoRunner" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
DatabaseName                   : ContosoRunner
ResourceGroupName              : ContosoRunnersProd
ServerName                     : runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="f22a6-110">Эта команда изменяет состояние автоматического выполнения для помощника с именем CreateIndex на Enabled.</span><span class="sxs-lookup"><span data-stu-id="f22a6-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="f22a6-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f22a6-111">PARAMETERS</span></span>

### <span data-ttu-id="f22a6-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="f22a6-112">-AdvisorName</span></span>
<span data-ttu-id="f22a6-113">Указывает имя помощника, для которого этот командлет изменяет состояние.</span><span class="sxs-lookup"><span data-stu-id="f22a6-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f22a6-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f22a6-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="f22a6-115">Задает значение состояния.</span><span class="sxs-lookup"><span data-stu-id="f22a6-115">Specifies the value for the status.</span></span>
<span data-ttu-id="f22a6-116">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f22a6-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f22a6-117">Включаем</span><span class="sxs-lookup"><span data-stu-id="f22a6-117">Enabled</span></span> 
- <span data-ttu-id="f22a6-118">Отключает</span><span class="sxs-lookup"><span data-stu-id="f22a6-118">Disabled</span></span> 
- <span data-ttu-id="f22a6-119">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="f22a6-119">Default</span></span>

```yaml
Type: AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f22a6-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f22a6-120">-DatabaseName</span></span>
<span data-ttu-id="f22a6-121">Указывает имя базы данных, для которой этот командлет изменяет состояние.</span><span class="sxs-lookup"><span data-stu-id="f22a6-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f22a6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f22a6-122">-DefaultProfile</span></span>
<span data-ttu-id="f22a6-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f22a6-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f22a6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f22a6-124">-ResourceGroupName</span></span>
<span data-ttu-id="f22a6-125">Указывает имя группы ресурсов для сервера, который содержит эту базу данных.</span><span class="sxs-lookup"><span data-stu-id="f22a6-125">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f22a6-126">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f22a6-126">-ServerName</span></span>
<span data-ttu-id="f22a6-127">Указывает имя сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="f22a6-127">Specifies the name of the server for the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f22a6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f22a6-128">-Confirm</span></span>
<span data-ttu-id="f22a6-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f22a6-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f22a6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f22a6-130">-WhatIf</span></span>
<span data-ttu-id="f22a6-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f22a6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f22a6-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f22a6-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f22a6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f22a6-133">CommonParameters</span></span>
<span data-ttu-id="f22a6-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f22a6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f22a6-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f22a6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f22a6-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f22a6-136">INPUTS</span></span>

### <span data-ttu-id="f22a6-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="f22a6-137">None</span></span>
<span data-ttu-id="f22a6-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f22a6-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f22a6-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f22a6-139">OUTPUTS</span></span>

### <span data-ttu-id="f22a6-140">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="f22a6-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>
<span data-ttu-id="f22a6-141">Этот командлет возвращает объект **AzureSqlDatabaseAdvisorModel** .</span><span class="sxs-lookup"><span data-stu-id="f22a6-141">This cmdlet returns an **AzureSqlDatabaseAdvisorModel** object.</span></span>

## <span data-ttu-id="f22a6-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="f22a6-142">NOTES</span></span>

## <span data-ttu-id="f22a6-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f22a6-143">RELATED LINKS</span></span>

[<span data-ttu-id="f22a6-144">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="f22a6-144">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="f22a6-145">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="f22a6-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

