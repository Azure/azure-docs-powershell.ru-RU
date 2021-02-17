---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: bd2a157a1fb05baf0fa6e02b061462718ffad314
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223028"
---
# <span data-ttu-id="4144e-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4144e-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="4144e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4144e-102">SYNOPSIS</span></span>
<span data-ttu-id="4144e-103">Возвращает или перечисляет группы отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="4144e-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="4144e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4144e-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4144e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4144e-105">DESCRIPTION</span></span>
<span data-ttu-id="4144e-106">Возвращает конкретную группу отбойных экземпляров или группы отбойных экземпляров в регионе, в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="4144e-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="4144e-107">Для выполнения команды может использоваться любая область в группе отбойных команд экземпляров.</span><span class="sxs-lookup"><span data-stu-id="4144e-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="4144e-108">Возвращаемые значения отражают состояние управляемых экземпляров в этом регионе в отношении группы отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="4144e-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="4144e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4144e-109">EXAMPLES</span></span>

### <span data-ttu-id="4144e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4144e-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location
Output:
{
    ResourceGroupName                     : rg
    Location                              : East US
    Name                                  : fg
    PartnerResourceGroupName              : rg
    PartnerRegion                         : West US
    PrimaryManagedInstanceName            : managedInstance1
    PartnerManagedInstanceName            : managedInstance2
    ReplicationRole                       : Primary
    ReplicationState                      : CATCH_UP
    ReadWriteFailoverPolicy               : Automatic
    FailoverWithDataLossGracePeriodHours  : 1
    ReadOnlyFailoverPolicy                : Disabled
    Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
}
```

<span data-ttu-id="4144e-111">Список всех групп отбойных передачи в регионе</span><span class="sxs-lookup"><span data-stu-id="4144e-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="4144e-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4144e-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="4144e-113">Получите определенную группу отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="4144e-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="4144e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4144e-114">PARAMETERS</span></span>

### <span data-ttu-id="4144e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4144e-115">-DefaultProfile</span></span>
<span data-ttu-id="4144e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4144e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4144e-117">-Location</span><span class="sxs-lookup"><span data-stu-id="4144e-117">-Location</span></span>
<span data-ttu-id="4144e-118">Имя локального региона, из которого нужно получить группу отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="4144e-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4144e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4144e-119">-Name</span></span>
<span data-ttu-id="4144e-120">Имя группы отбойных экземпляров, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="4144e-120">The name of the Instance Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4144e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4144e-121">-ResourceGroupName</span></span>
<span data-ttu-id="4144e-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4144e-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4144e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4144e-123">CommonParameters</span></span>
<span data-ttu-id="4144e-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4144e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4144e-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4144e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4144e-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4144e-126">INPUTS</span></span>

### <span data-ttu-id="4144e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="4144e-127">System.String</span></span>

## <span data-ttu-id="4144e-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4144e-128">OUTPUTS</span></span>

### <span data-ttu-id="4144e-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="4144e-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="4144e-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4144e-130">NOTES</span></span>

## <span data-ttu-id="4144e-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4144e-131">RELATED LINKS</span></span>
