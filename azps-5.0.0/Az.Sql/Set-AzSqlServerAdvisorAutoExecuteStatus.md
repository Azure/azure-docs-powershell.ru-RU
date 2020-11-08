---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 02a4348511afabe7f398eafeb6d0849525f0abac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246960"
---
# <span data-ttu-id="b4148-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b4148-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="b4148-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4148-102">SYNOPSIS</span></span>
<span data-ttu-id="b4148-103">Обновляет состояние автоматического выполнения советника SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="b4148-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="b4148-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4148-104">SYNTAX</span></span>

```
Set-AzSqlServerAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4148-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4148-105">DESCRIPTION</span></span>
<span data-ttu-id="b4148-106">Командлет **Set-AzSqlServerAdvisorAutoExecuteStatus** задает свойство автоматического выполнения для советника SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="b4148-106">The **Set-AzSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="b4148-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4148-107">EXAMPLES</span></span>

### <span data-ttu-id="b4148-108">Пример 1: Включение автоматического выполнения для помощника</span><span class="sxs-lookup"><span data-stu-id="b4148-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
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

<span data-ttu-id="b4148-109">Эта команда включает состояние автоматического выполнения для помощника с именем CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="b4148-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="b4148-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4148-110">PARAMETERS</span></span>

### <span data-ttu-id="b4148-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="b4148-111">-AdvisorName</span></span>
<span data-ttu-id="b4148-112">Указывает имя помощника, для которого этот командлет обновляет состояние автоматического выполнения.</span><span class="sxs-lookup"><span data-stu-id="b4148-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="b4148-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b4148-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="b4148-114">Указывает значение, на которое этот командлет обновляет состояние автоматического выполнения.</span><span class="sxs-lookup"><span data-stu-id="b4148-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="b4148-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b4148-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b4148-116">Включаем</span><span class="sxs-lookup"><span data-stu-id="b4148-116">Enabled</span></span>
- <span data-ttu-id="b4148-117">Отключает</span><span class="sxs-lookup"><span data-stu-id="b4148-117">Disabled</span></span>
- <span data-ttu-id="b4148-118">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="b4148-118">Default</span></span>

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

### <span data-ttu-id="b4148-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4148-119">-DefaultProfile</span></span>
<span data-ttu-id="b4148-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b4148-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4148-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4148-121">-ResourceGroupName</span></span>
<span data-ttu-id="b4148-122">Указывает имя группы ресурсов сервера.</span><span class="sxs-lookup"><span data-stu-id="b4148-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="b4148-123">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="b4148-123">-ServerName</span></span>
<span data-ttu-id="b4148-124">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="b4148-124">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="b4148-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4148-125">-Confirm</span></span>
<span data-ttu-id="b4148-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b4148-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4148-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4148-127">-WhatIf</span></span>
<span data-ttu-id="b4148-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b4148-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4148-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b4148-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4148-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4148-130">CommonParameters</span></span>
<span data-ttu-id="b4148-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4148-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4148-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4148-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4148-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4148-133">INPUTS</span></span>

### <span data-ttu-id="b4148-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b4148-134">System.String</span></span>

### <span data-ttu-id="b4148-135">Microsoft. Azure. Commands. SQL. Advisor. командлет. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b4148-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="b4148-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4148-136">OUTPUTS</span></span>

### <span data-ttu-id="b4148-137">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="b4148-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="b4148-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4148-138">NOTES</span></span>
* <span data-ttu-id="b4148-139">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, сервер</span><span class="sxs-lookup"><span data-stu-id="b4148-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="b4148-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4148-140">RELATED LINKS</span></span>

[<span data-ttu-id="b4148-141">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="b4148-141">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="b4148-142">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="b4148-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
