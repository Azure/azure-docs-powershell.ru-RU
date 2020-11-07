---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: f1ba6e50c03fffbd4eb6407e90e2a50957806539
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912436"
---
# <span data-ttu-id="c7be6-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="c7be6-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="c7be6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7be6-102">SYNOPSIS</span></span>
<span data-ttu-id="c7be6-103">Получение одного или нескольких прослушивателей групп доступности в группе виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="c7be6-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="c7be6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7be6-104">SYNTAX</span></span>

### <span data-ttu-id="c7be6-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c7be6-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7be6-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="c7be6-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7be6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7be6-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7be6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7be6-108">DESCRIPTION</span></span>
<span data-ttu-id="c7be6-109">Get-AzAvailabilityGroupListener получает один или несколько прослушивателей групп доступности из группы виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="c7be6-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="c7be6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7be6-110">EXAMPLES</span></span>

### <span data-ttu-id="c7be6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c7be6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="c7be6-112">Name ResourceGroupName имя_группы AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="c7be6-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="c7be6-113">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="c7be6-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="c7be6-114">Эта команда получает сведения о AgListener01 прослушивателя группы доступности в группе SqlVmGroup01 и ResourceGroup01 ресурсов для виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="c7be6-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="c7be6-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c7be6-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="c7be6-116">Name ResourceGroupName имя_группы AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="c7be6-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="c7be6-117">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="c7be6-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="c7be6-118">Эта команда получает сведения обо всех прослушивателях групп доступности в группе SqlVmGroup01 и ResourceGroup01 группы ресурсов для виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="c7be6-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="c7be6-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c7be6-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="c7be6-120">Name ResourceGroupName имя_группы AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="c7be6-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="c7be6-121">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="c7be6-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="c7be6-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7be6-122">PARAMETERS</span></span>

### <span data-ttu-id="c7be6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7be6-123">-DefaultProfile</span></span>
<span data-ttu-id="c7be6-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7be6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7be6-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c7be6-125">-Name</span></span>
<span data-ttu-id="c7be6-126">Имя прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="c7be6-126">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="c7be6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7be6-127">-ResourceGroupName</span></span>
<span data-ttu-id="c7be6-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c7be6-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="c7be6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7be6-129">-ResourceId</span></span>
<span data-ttu-id="c7be6-130">Идентификатор ресурса прослушивателя группы доступности</span><span class="sxs-lookup"><span data-stu-id="c7be6-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="c7be6-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="c7be6-131">-SqlVMGroupName</span></span>
<span data-ttu-id="c7be6-132">Имя группы виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="c7be6-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="c7be6-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="c7be6-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="c7be6-134">Объект группы виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="c7be6-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="c7be6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7be6-135">CommonParameters</span></span>
<span data-ttu-id="c7be6-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7be6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7be6-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7be6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7be6-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7be6-138">INPUTS</span></span>

### <span data-ttu-id="c7be6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c7be6-139">System.String</span></span>

### <span data-ttu-id="c7be6-140">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="c7be6-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="c7be6-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7be6-141">OUTPUTS</span></span>

### <span data-ttu-id="c7be6-142">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="c7be6-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="c7be6-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7be6-143">NOTES</span></span>

## <span data-ttu-id="c7be6-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7be6-144">RELATED LINKS</span></span>
