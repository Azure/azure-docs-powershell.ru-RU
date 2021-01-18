---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
ms.openlocfilehash: e53857533770d6de0040d2d777020f1a2f9f320a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507626"
---
# <span data-ttu-id="97b3c-101">Get-AzSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="97b3c-101">Get-AzSqlServerServiceObjective</span></span>

## <span data-ttu-id="97b3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97b3c-102">SYNOPSIS</span></span>
<span data-ttu-id="97b3c-103">Получает цели обслуживания для сервера базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="97b3c-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="97b3c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="97b3c-104">SYNTAX</span></span>

### <span data-ttu-id="97b3c-105">ByLocation (Default)</span><span class="sxs-lookup"><span data-stu-id="97b3c-105">ByLocation (Default)</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97b3c-106">ByServer</span><span class="sxs-lookup"><span data-stu-id="97b3c-106">ByServer</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ResourceGroupName] <String>
 [-ServerName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97b3c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97b3c-107">DESCRIPTION</span></span>
<span data-ttu-id="97b3c-108">Для сервера базы данных Azure SQL целей службы **get-AzSqlServerServiceObjective.**</span><span class="sxs-lookup"><span data-stu-id="97b3c-108">The **Get-AzSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="97b3c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="97b3c-109">EXAMPLES</span></span>

### <span data-ttu-id="97b3c-110">Пример 1. Цели обслуживания</span><span class="sxs-lookup"><span data-stu-id="97b3c-110">Example 1: Get service objectives</span></span>
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

<span data-ttu-id="97b3c-111">Эта команда служит для целей обслуживания сервера Server01.</span><span class="sxs-lookup"><span data-stu-id="97b3c-111">This command gets the service objectives for the server named Server01.</span></span>

### <span data-ttu-id="97b3c-112">Пример 2. Цели работы службы с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="97b3c-112">Example 2: Get service objectives using filtering</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServiceObjectiveName "P*"
ServiceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
```

<span data-ttu-id="97b3c-113">Эта команда служит для целей обслуживания сервера Server01, которые начинаются с "Система".</span><span class="sxs-lookup"><span data-stu-id="97b3c-113">This command gets the service objectives for the server named Server01 that start with "System".</span></span>

### <span data-ttu-id="97b3c-114">Пример 3. Получить цели обслуживания для расположения</span><span class="sxs-lookup"><span data-stu-id="97b3c-114">Example 3: Get service objectives for a location</span></span>
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

<span data-ttu-id="97b3c-115">Эта команда получает цели обслуживания для указанного региона Azure.</span><span class="sxs-lookup"><span data-stu-id="97b3c-115">This command gets the service objectives for a specified Azure region.</span></span>

## <span data-ttu-id="97b3c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97b3c-116">PARAMETERS</span></span>

### <span data-ttu-id="97b3c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b3c-117">-DefaultProfile</span></span>
<span data-ttu-id="97b3c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="97b3c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97b3c-119">-Location</span><span class="sxs-lookup"><span data-stu-id="97b3c-119">-Location</span></span>
<span data-ttu-id="97b3c-120">Название расположения, для которого нужно получить цели обслуживания.</span><span class="sxs-lookup"><span data-stu-id="97b3c-120">The name of the Location for which to get the service objectives.</span></span>

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

### <span data-ttu-id="97b3c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97b3c-121">-ResourceGroupName</span></span>
<span data-ttu-id="97b3c-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97b3c-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="97b3c-123">Этот cmdlet получает цели обслуживания для сервера SQL базы данных, назначенного этому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="97b3c-123">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="97b3c-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="97b3c-124">-ServerName</span></span>
<span data-ttu-id="97b3c-125">Указывает имя сервера SQL базы SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="97b3c-125">Specifies the name of a SQL Database SQL Database server.</span></span>

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

### <span data-ttu-id="97b3c-126">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="97b3c-126">-ServiceObjectiveName</span></span>
<span data-ttu-id="97b3c-127">Указывает имя цели обслуживания для сервера базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="97b3c-127">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="97b3c-128">Допустимые значения этого параметра: Basic, S0, S1, S2, P1, P2 и P3.</span><span class="sxs-lookup"><span data-stu-id="97b3c-128">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

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

### <span data-ttu-id="97b3c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97b3c-129">-Confirm</span></span>
<span data-ttu-id="97b3c-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="97b3c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97b3c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97b3c-131">-WhatIf</span></span>
<span data-ttu-id="97b3c-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97b3c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97b3c-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="97b3c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97b3c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b3c-134">CommonParameters</span></span>
<span data-ttu-id="97b3c-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97b3c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b3c-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97b3c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b3c-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97b3c-137">INPUTS</span></span>

### <span data-ttu-id="97b3c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="97b3c-138">System.String</span></span>

## <span data-ttu-id="97b3c-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="97b3c-139">OUTPUTS</span></span>

### <span data-ttu-id="97b3c-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="97b3c-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="97b3c-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="97b3c-141">NOTES</span></span>

## <span data-ttu-id="97b3c-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97b3c-142">RELATED LINKS</span></span>

[<span data-ttu-id="97b3c-143">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="97b3c-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


