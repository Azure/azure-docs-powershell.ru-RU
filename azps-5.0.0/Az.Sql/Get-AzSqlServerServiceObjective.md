---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
ms.openlocfilehash: e53857533770d6de0040d2d777020f1a2f9f320a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249423"
---
# <span data-ttu-id="4657a-101">Get-AzSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="4657a-101">Get-AzSqlServerServiceObjective</span></span>

## <span data-ttu-id="4657a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4657a-102">SYNOPSIS</span></span>
<span data-ttu-id="4657a-103">Получение целей обслуживания для сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4657a-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="4657a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4657a-104">SYNTAX</span></span>

### <span data-ttu-id="4657a-105">ByLocation (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4657a-105">ByLocation (Default)</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4657a-106">ByServer</span><span class="sxs-lookup"><span data-stu-id="4657a-106">ByServer</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ResourceGroupName] <String>
 [-ServerName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4657a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4657a-107">DESCRIPTION</span></span>
<span data-ttu-id="4657a-108">Командлет **Get-AzSqlServerServiceObjective** получает доступные цели обслуживания для сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4657a-108">The **Get-AzSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="4657a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4657a-109">EXAMPLES</span></span>

### <span data-ttu-id="4657a-110">Пример 1: получение целей обслуживания</span><span class="sxs-lookup"><span data-stu-id="4657a-110">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="4657a-111">Эта команда получает цели службы для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="4657a-111">This command gets the service objectives for the server named Server01.</span></span>

### <span data-ttu-id="4657a-112">Пример 2: получение целей обслуживания с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="4657a-112">Example 2: Get service objectives using filtering</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServiceObjectiveName "P*"
ServiceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
```

<span data-ttu-id="4657a-113">Эта команда получает цели службы для сервера с именем Server01, который начинается со слова System.</span><span class="sxs-lookup"><span data-stu-id="4657a-113">This command gets the service objectives for the server named Server01 that start with "System".</span></span>

### <span data-ttu-id="4657a-114">Пример 3: получение целей обслуживания для местоположения</span><span class="sxs-lookup"><span data-stu-id="4657a-114">Example 3: Get service objectives for a location</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -Location "west us"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="4657a-115">Эта команда получает цели службы для определенного региона Azure.</span><span class="sxs-lookup"><span data-stu-id="4657a-115">This command gets the service objectives for a specified Azure region.</span></span>

## <span data-ttu-id="4657a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4657a-116">PARAMETERS</span></span>

### <span data-ttu-id="4657a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4657a-117">-DefaultProfile</span></span>
<span data-ttu-id="4657a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4657a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4657a-119">-Location</span><span class="sxs-lookup"><span data-stu-id="4657a-119">-Location</span></span>
<span data-ttu-id="4657a-120">Имя расположения, для которого требуется получить цели службы.</span><span class="sxs-lookup"><span data-stu-id="4657a-120">The name of the Location for which to get the service objectives.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4657a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4657a-121">-ResourceGroupName</span></span>
<span data-ttu-id="4657a-122">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4657a-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="4657a-123">Этот командлет получает цели службы для сервера базы данных SQL, назначенного этому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="4657a-123">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4657a-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="4657a-124">-ServerName</span></span>
<span data-ttu-id="4657a-125">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="4657a-125">Specifies the name of a SQL Database SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4657a-126">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="4657a-126">-ServiceObjectiveName</span></span>
<span data-ttu-id="4657a-127">Указывает имя цели обслуживания для сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4657a-127">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="4657a-128">Допустимые значения этого параметра: Basic, S0, S1, S2, P1, P2 и P3.</span><span class="sxs-lookup"><span data-stu-id="4657a-128">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4657a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4657a-129">-Confirm</span></span>
<span data-ttu-id="4657a-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4657a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4657a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4657a-131">-WhatIf</span></span>
<span data-ttu-id="4657a-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4657a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4657a-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4657a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4657a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4657a-134">CommonParameters</span></span>
<span data-ttu-id="4657a-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4657a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4657a-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4657a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4657a-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4657a-137">INPUTS</span></span>

### <span data-ttu-id="4657a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4657a-138">System.String</span></span>

## <span data-ttu-id="4657a-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4657a-139">OUTPUTS</span></span>

### <span data-ttu-id="4657a-140">Microsoft. Azure. Commands. SQL. ServiceObjective. Model. AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="4657a-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="4657a-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="4657a-141">NOTES</span></span>

## <span data-ttu-id="4657a-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4657a-142">RELATED LINKS</span></span>

[<span data-ttu-id="4657a-143">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="4657a-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

