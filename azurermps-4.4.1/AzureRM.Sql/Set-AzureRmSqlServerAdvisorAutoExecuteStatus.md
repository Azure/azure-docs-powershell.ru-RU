---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: f483d3deb6c4e4ee6fb5c091dffc9b7969766d6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566266"
---
# <span data-ttu-id="927dd-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="927dd-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="927dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="927dd-102">SYNOPSIS</span></span>
<span data-ttu-id="927dd-103">Обновляет состояние автоматического выполнения советника SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="927dd-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="927dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="927dd-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="927dd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="927dd-105">DESCRIPTION</span></span>
<span data-ttu-id="927dd-106">Командлет **Set-AzureRmSqlServerAdvisorAutoExecuteStatus** задает свойство автоматического выполнения для советника SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="927dd-106">The **Set-AzureRmSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="927dd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="927dd-107">EXAMPLES</span></span>

### <span data-ttu-id="927dd-108">Пример 1: Включение автоматического выполнения для помощника</span><span class="sxs-lookup"><span data-stu-id="927dd-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzureRmSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Server
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="927dd-109">Эта команда включает состояние автоматического выполнения для помощника с именем CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="927dd-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="927dd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="927dd-110">PARAMETERS</span></span>

### <span data-ttu-id="927dd-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="927dd-111">-AdvisorName</span></span>
<span data-ttu-id="927dd-112">Указывает имя помощника, для которого этот командлет обновляет состояние автоматического выполнения.</span><span class="sxs-lookup"><span data-stu-id="927dd-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="927dd-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="927dd-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="927dd-114">Указывает значение, на которое этот командлет обновляет состояние автоматического выполнения.</span><span class="sxs-lookup"><span data-stu-id="927dd-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="927dd-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="927dd-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="927dd-116">Включаем</span><span class="sxs-lookup"><span data-stu-id="927dd-116">Enabled</span></span>
- <span data-ttu-id="927dd-117">Отключает</span><span class="sxs-lookup"><span data-stu-id="927dd-117">Disabled</span></span>
- <span data-ttu-id="927dd-118">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="927dd-118">Default</span></span>

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

### <span data-ttu-id="927dd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="927dd-119">-ResourceGroupName</span></span>
<span data-ttu-id="927dd-120">Указывает имя группы ресурсов сервера.</span><span class="sxs-lookup"><span data-stu-id="927dd-120">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="927dd-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="927dd-121">-ServerName</span></span>
<span data-ttu-id="927dd-122">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="927dd-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="927dd-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="927dd-123">-Confirm</span></span>
<span data-ttu-id="927dd-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="927dd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="927dd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="927dd-125">-WhatIf</span></span>
<span data-ttu-id="927dd-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="927dd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="927dd-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="927dd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="927dd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="927dd-128">-DefaultProfile</span></span>
<span data-ttu-id="927dd-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="927dd-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="927dd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="927dd-130">CommonParameters</span></span>
<span data-ttu-id="927dd-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="927dd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="927dd-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="927dd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="927dd-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="927dd-133">INPUTS</span></span>

## <span data-ttu-id="927dd-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="927dd-134">OUTPUTS</span></span>

### <span data-ttu-id="927dd-135">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="927dd-135">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="927dd-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="927dd-136">NOTES</span></span>
* <span data-ttu-id="927dd-137">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, сервер</span><span class="sxs-lookup"><span data-stu-id="927dd-137">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="927dd-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="927dd-138">RELATED LINKS</span></span>

[<span data-ttu-id="927dd-139">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="927dd-139">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="927dd-140">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="927dd-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
