---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 2b8ddc8b15ca9fa7322de231f9688548c4073708
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014776"
---
# <span data-ttu-id="c1fe6-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c1fe6-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="c1fe6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1fe6-102">SYNOPSIS</span></span>
<span data-ttu-id="c1fe6-103">Возвращает или перечисляет группы отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="c1fe6-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="c1fe6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c1fe6-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1fe6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1fe6-105">DESCRIPTION</span></span>
<span data-ttu-id="c1fe6-106">Возвращает конкретную группу отбойных экземпляров или группы отбойных экземпляров в регионе, в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="c1fe6-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="c1fe6-107">Для выполнения команды может использоваться любая область в группе отбойных команд экземпляров.</span><span class="sxs-lookup"><span data-stu-id="c1fe6-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="c1fe6-108">Возвращаемые значения отражают состояние управляемых экземпляров в этом регионе в отношении группы отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="c1fe6-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="c1fe6-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c1fe6-109">EXAMPLES</span></span>

### <span data-ttu-id="c1fe6-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c1fe6-110">Example 1</span></span>
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

<span data-ttu-id="c1fe6-111">Список всех групп отбойных передачи в регионе</span><span class="sxs-lookup"><span data-stu-id="c1fe6-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="c1fe6-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c1fe6-112">Example 2</span></span>
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

<span data-ttu-id="c1fe6-113">Получите определенную группу отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="c1fe6-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="c1fe6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1fe6-114">PARAMETERS</span></span>

### <span data-ttu-id="c1fe6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1fe6-115">-DefaultProfile</span></span>
<span data-ttu-id="c1fe6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1fe6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1fe6-117">-Location</span><span class="sxs-lookup"><span data-stu-id="c1fe6-117">-Location</span></span>
<span data-ttu-id="c1fe6-118">Имя локального региона, из которого нужно получить группу отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="c1fe6-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="c1fe6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c1fe6-119">-Name</span></span>
<span data-ttu-id="c1fe6-120">Имя группы отбойных экземпляров, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="c1fe6-120">The name of the Instance Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="c1fe6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1fe6-121">-ResourceGroupName</span></span>
<span data-ttu-id="c1fe6-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c1fe6-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="c1fe6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1fe6-123">CommonParameters</span></span>
<span data-ttu-id="c1fe6-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1fe6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1fe6-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1fe6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1fe6-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1fe6-126">INPUTS</span></span>

### <span data-ttu-id="c1fe6-127">System.String</span><span class="sxs-lookup"><span data-stu-id="c1fe6-127">System.String</span></span>

## <span data-ttu-id="c1fe6-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c1fe6-128">OUTPUTS</span></span>

### <span data-ttu-id="c1fe6-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="c1fe6-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="c1fe6-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c1fe6-130">NOTES</span></span>

## <span data-ttu-id="c1fe6-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1fe6-131">RELATED LINKS</span></span>
