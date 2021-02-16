---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: f1ba6e50c03fffbd4eb6407e90e2a50957806539
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229937"
---
# <span data-ttu-id="5cb81-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="5cb81-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="5cb81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cb81-102">SYNOPSIS</span></span>
<span data-ttu-id="5cb81-103">Получите одну или несколько групп доступности в группе SQL виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="5cb81-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="5cb81-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5cb81-104">SYNTAX</span></span>

### <span data-ttu-id="5cb81-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5cb81-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cb81-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="5cb81-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cb81-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cb81-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5cb81-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cb81-108">DESCRIPTION</span></span>
<span data-ttu-id="5cb81-109">Этот Get-AzAvailabilityGroupListener получает одного или несколько слушателей группы доступности из SQL Virtual Machine Group.</span><span class="sxs-lookup"><span data-stu-id="5cb81-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="5cb81-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5cb81-110">EXAMPLES</span></span>

### <span data-ttu-id="5cb81-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5cb81-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="5cb81-112">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="5cb81-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="5cb81-113">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="5cb81-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="5cb81-114">Эта команда получает сведения о прослушке группы доступности AgListener01 в группе SQL Virtual Machine Group SqlVmGroup01 и Resource Group ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="5cb81-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="5cb81-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5cb81-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="5cb81-116">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="5cb81-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="5cb81-117">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="5cb81-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="5cb81-118">Эта команда получает сведения обо всех группах доступности в SQL Группа виртуальных машин SqlVmGroup01 и Resource Group ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="5cb81-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="5cb81-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5cb81-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="5cb81-120">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="5cb81-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="5cb81-121">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="5cb81-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="5cb81-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cb81-122">PARAMETERS</span></span>

### <span data-ttu-id="5cb81-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cb81-123">-DefaultProfile</span></span>
<span data-ttu-id="5cb81-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5cb81-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cb81-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5cb81-125">-Name</span></span>
<span data-ttu-id="5cb81-126">Имя прослушавщика группы доступности.</span><span class="sxs-lookup"><span data-stu-id="5cb81-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cb81-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cb81-127">-ResourceGroupName</span></span>
<span data-ttu-id="5cb81-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5cb81-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cb81-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cb81-129">-ResourceId</span></span>
<span data-ttu-id="5cb81-130">ИД ресурса группы «Доступность»</span><span class="sxs-lookup"><span data-stu-id="5cb81-130">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cb81-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="5cb81-131">-SqlVMGroupName</span></span>
<span data-ttu-id="5cb81-132">SQL группы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="5cb81-132">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cb81-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="5cb81-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="5cb81-134">SQL группа виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="5cb81-134">SQL virtual machine Group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cb81-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb81-135">CommonParameters</span></span>
<span data-ttu-id="5cb81-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cb81-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb81-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5cb81-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb81-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5cb81-138">INPUTS</span></span>

### <span data-ttu-id="5cb81-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5cb81-139">System.String</span></span>

### <span data-ttu-id="5cb81-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMaviree.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="5cb81-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="5cb81-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5cb81-141">OUTPUTS</span></span>

### <span data-ttu-id="5cb81-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="5cb81-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="5cb81-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5cb81-143">NOTES</span></span>

## <span data-ttu-id="5cb81-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5cb81-144">RELATED LINKS</span></span>
