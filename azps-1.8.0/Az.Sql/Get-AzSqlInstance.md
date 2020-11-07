---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
ms.openlocfilehash: a21b2436f44cb2df5f9984e70ccecf6c1d9c306a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728979"
---
# <span data-ttu-id="7b933-101">Get-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7b933-101">Get-AzSqlInstance</span></span>

## <span data-ttu-id="7b933-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7b933-102">SYNOPSIS</span></span>
<span data-ttu-id="7b933-103">Возвращает сведения о экземпляре управляемой базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7b933-103">Returns information about Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="7b933-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7b933-104">SYNTAX</span></span>

```
Get-AzSqlInstance [[-Name] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b933-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b933-105">DESCRIPTION</span></span>
<span data-ttu-id="7b933-106">Командлет **Get-AzSqlInstance** возвращает сведения об одном или нескольких экземплярах, УПРАВЛЯЕМЫХ Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7b933-106">The **Get-AzSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="7b933-107">Укажите имя экземпляра, чтобы просмотреть сведения только для этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7b933-107">Specify the name of a instance to see information for only that instance.</span></span>

## <span data-ttu-id="7b933-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7b933-108">EXAMPLES</span></span>

### <span data-ttu-id="7b933-109">Пример 1: получение всех экземпляров, назначенных группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="7b933-109">Example 1: Get all instances assigned to a resource group</span></span>
```
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="7b933-110">Эта команда получает сведения обо всех экземплярах, назначенных группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="7b933-110">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="7b933-111">Пример 2: получение сведений о экземпляре</span><span class="sxs-lookup"><span data-stu-id="7b933-111">Example 2: Get information about an  instance</span></span>
```
PS C:\> Get-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="7b933-112">Эта команда получает сведения о экземпляре с именем managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="7b933-112">This command gets information about the instance named managedInstance1.</span></span>

### <span data-ttu-id="7b933-113">Пример 3: получение всех экземпляров, назначенных группе ресурсов с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="7b933-113">Example 3: Get all instances assigned to a resource group using filtering</span></span>
```
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "managedInstance*"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="7b933-114">Эта команда получает сведения обо всех экземплярах, назначенных группе ресурсов ResourceGroup01, которая начинается с "managedInstance".</span><span class="sxs-lookup"><span data-stu-id="7b933-114">This command gets information about all instances assigned to the resource group ResourceGroup01 that start with "managedInstance".</span></span>

## <span data-ttu-id="7b933-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7b933-115">PARAMETERS</span></span>

### <span data-ttu-id="7b933-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b933-116">-DefaultProfile</span></span>
<span data-ttu-id="7b933-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b933-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b933-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7b933-118">-Name</span></span>
<span data-ttu-id="7b933-119">Имя экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="7b933-119">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="7b933-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b933-120">-ResourceGroupName</span></span>
<span data-ttu-id="7b933-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7b933-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="7b933-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b933-122">CommonParameters</span></span>
<span data-ttu-id="7b933-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7b933-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b933-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b933-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b933-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7b933-125">INPUTS</span></span>

### <span data-ttu-id="7b933-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="7b933-126">None</span></span>

## <span data-ttu-id="7b933-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b933-127">OUTPUTS</span></span>

### <span data-ttu-id="7b933-128">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="7b933-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="7b933-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="7b933-129">NOTES</span></span>

## <span data-ttu-id="7b933-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b933-130">RELATED LINKS</span></span>
