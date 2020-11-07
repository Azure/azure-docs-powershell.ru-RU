---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: ad64246d51e2f590ab19d93fd08fdd2a02943afd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733944"
---
# <span data-ttu-id="a8aae-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="a8aae-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="a8aae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8aae-102">SYNOPSIS</span></span>
<span data-ttu-id="a8aae-103">Обновляет состояние автоматического выполнения советника SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="a8aae-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8aae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8aae-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8aae-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8aae-105">DESCRIPTION</span></span>
<span data-ttu-id="a8aae-106">Командлет **Set-AzureRmSqlServerAdvisorAutoExecuteStatus** задает свойство автоматического выполнения для советника SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="a8aae-106">The **Set-AzureRmSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="a8aae-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8aae-107">EXAMPLES</span></span>

### <span data-ttu-id="a8aae-108">Пример 1: Включение автоматического выполнения для помощника</span><span class="sxs-lookup"><span data-stu-id="a8aae-108">Example 1: Enable auto execute for an Advisor</span></span>
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

<span data-ttu-id="a8aae-109">Эта команда включает состояние автоматического выполнения для помощника с именем CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="a8aae-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="a8aae-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8aae-110">PARAMETERS</span></span>

### <span data-ttu-id="a8aae-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="a8aae-111">-AdvisorName</span></span>
<span data-ttu-id="a8aae-112">Указывает имя помощника, для которого этот командлет обновляет состояние автоматического выполнения.</span><span class="sxs-lookup"><span data-stu-id="a8aae-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="a8aae-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="a8aae-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="a8aae-114">Указывает значение, на которое этот командлет обновляет состояние автоматического выполнения.</span><span class="sxs-lookup"><span data-stu-id="a8aae-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="a8aae-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a8aae-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a8aae-116">Включаем</span><span class="sxs-lookup"><span data-stu-id="a8aae-116">Enabled</span></span>
- <span data-ttu-id="a8aae-117">Отключает</span><span class="sxs-lookup"><span data-stu-id="a8aae-117">Disabled</span></span>
- <span data-ttu-id="a8aae-118">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8aae-118">Default</span></span>

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

### <span data-ttu-id="a8aae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8aae-119">-DefaultProfile</span></span>
<span data-ttu-id="a8aae-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a8aae-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8aae-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8aae-121">-ResourceGroupName</span></span>
<span data-ttu-id="a8aae-122">Указывает имя группы ресурсов сервера.</span><span class="sxs-lookup"><span data-stu-id="a8aae-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="a8aae-123">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="a8aae-123">-ServerName</span></span>
<span data-ttu-id="a8aae-124">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="a8aae-124">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="a8aae-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8aae-125">-Confirm</span></span>
<span data-ttu-id="a8aae-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a8aae-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8aae-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8aae-127">-WhatIf</span></span>
<span data-ttu-id="a8aae-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a8aae-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8aae-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a8aae-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8aae-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8aae-130">CommonParameters</span></span>
<span data-ttu-id="a8aae-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8aae-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8aae-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8aae-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8aae-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8aae-133">INPUTS</span></span>

### <span data-ttu-id="a8aae-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="a8aae-134">None</span></span>
<span data-ttu-id="a8aae-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a8aae-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a8aae-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8aae-136">OUTPUTS</span></span>

### <span data-ttu-id="a8aae-137">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="a8aae-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="a8aae-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8aae-138">NOTES</span></span>
* <span data-ttu-id="a8aae-139">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, сервер</span><span class="sxs-lookup"><span data-stu-id="a8aae-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="a8aae-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8aae-140">RELATED LINKS</span></span>

[<span data-ttu-id="a8aae-141">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="a8aae-141">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="a8aae-142">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="a8aae-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
