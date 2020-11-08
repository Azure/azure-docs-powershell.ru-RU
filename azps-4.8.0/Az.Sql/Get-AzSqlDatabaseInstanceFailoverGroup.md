---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: bd2a157a1fb05baf0fa6e02b061462718ffad314
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078697"
---
# <span data-ttu-id="15300-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="15300-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="15300-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15300-102">SYNOPSIS</span></span>
<span data-ttu-id="15300-103">Возвращает или перечисляет группы отработки отказа для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="15300-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="15300-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15300-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15300-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15300-105">DESCRIPTION</span></span>
<span data-ttu-id="15300-106">Возвращает определенную группу отработки отказа для экземпляра или список групп отработки отказа экземпляров в регионе под подпиской пользователя.</span><span class="sxs-lookup"><span data-stu-id="15300-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="15300-107">Для выполнения команды может использоваться любой регион в группе отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="15300-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="15300-108">Возвращенные значения будут отражать состояние управляемых экземпляров в этой области относительно группы отработки отказа для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="15300-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="15300-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15300-109">EXAMPLES</span></span>

### <span data-ttu-id="15300-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="15300-110">Example 1</span></span>
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

<span data-ttu-id="15300-111">Список всех групп, отработок отказа в регионе</span><span class="sxs-lookup"><span data-stu-id="15300-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="15300-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="15300-112">Example 2</span></span>
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

<span data-ttu-id="15300-113">Получить определенную группу отработки отказа для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="15300-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="15300-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15300-114">PARAMETERS</span></span>

### <span data-ttu-id="15300-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15300-115">-DefaultProfile</span></span>
<span data-ttu-id="15300-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15300-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15300-117">-Location</span><span class="sxs-lookup"><span data-stu-id="15300-117">-Location</span></span>
<span data-ttu-id="15300-118">Имя локальной области, из которой извлекается группа отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="15300-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="15300-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="15300-119">-Name</span></span>
<span data-ttu-id="15300-120">Имя группы отработки отказа для извлекаемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="15300-120">The name of the Instance Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="15300-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15300-121">-ResourceGroupName</span></span>
<span data-ttu-id="15300-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="15300-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="15300-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15300-123">CommonParameters</span></span>
<span data-ttu-id="15300-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15300-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15300-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15300-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15300-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15300-126">INPUTS</span></span>

### <span data-ttu-id="15300-127">System. String</span><span class="sxs-lookup"><span data-stu-id="15300-127">System.String</span></span>

## <span data-ttu-id="15300-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15300-128">OUTPUTS</span></span>

### <span data-ttu-id="15300-129">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="15300-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="15300-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="15300-130">NOTES</span></span>

## <span data-ttu-id="15300-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15300-131">RELATED LINKS</span></span>