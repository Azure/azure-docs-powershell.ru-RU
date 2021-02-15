---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudService.md
ms.openlocfilehash: faab9e645f05b8b661b03911bcba517e770f4d78
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239103"
---
# <span data-ttu-id="de586-101">Get-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="de586-101">Get-AzCloudService</span></span>

## <span data-ttu-id="de586-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de586-102">SYNOPSIS</span></span>
<span data-ttu-id="de586-103">Отображение сведений об облачной службе.</span><span class="sxs-lookup"><span data-stu-id="de586-103">Display information about a cloud service.</span></span>

## <span data-ttu-id="de586-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="de586-104">SYNTAX</span></span>

### <span data-ttu-id="de586-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="de586-105">List (Default)</span></span>
```
Get-AzCloudService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="de586-106">Получить</span><span class="sxs-lookup"><span data-stu-id="de586-106">Get</span></span>
```
Get-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="de586-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="de586-107">GetViaIdentity</span></span>
```
Get-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="de586-108">Список1</span><span class="sxs-lookup"><span data-stu-id="de586-108">List1</span></span>
```
Get-AzCloudService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="de586-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de586-109">DESCRIPTION</span></span>
<span data-ttu-id="de586-110">Отображение сведений об облачной службе.</span><span class="sxs-lookup"><span data-stu-id="de586-110">Display information about a cloud service.</span></span>

## <span data-ttu-id="de586-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="de586-111">EXAMPLES</span></span>

### <span data-ttu-id="de586-112">Пример 1. Получить все облачные службы в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="de586-112">Example 1: Get all cloud service under a resource group</span></span>
```powershell
PS C:\> Get-AzCloudService -ResourceGroupName "ContosOrg"

ResourceGroupName Name              Location    ProvisioningState
----------------- ----              --------    -----------------
ContosOrg         ContosoCS         eastus2euap Succeeded
ContosOrg         ContosoCSTest     eastus2euap Failed
```

<span data-ttu-id="de586-113">Эта команда возвращает все облачные службы в группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="de586-113">This command gets all cloud services in resource group named ContosOrg</span></span>

### <span data-ttu-id="de586-114">Пример 2. Получить облачную службу</span><span class="sxs-lookup"><span data-stu-id="de586-114">Example 2: Get cloud service</span></span>
```powershell
PS C:\> Get-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

ResourceGroupName Name              Location    ProvisioningState
----------------- ----              --------    -----------------
ContosOrg         ContosoCS         eastus2euap Succeeded

PS C:\> $cloudService = Get-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
PS C:\> $cloudService | Format-List
ResourceGroupName : ContosOrg
Configuration     : xxxxxxxx
ConfigurationUrl  :
ExtensionProfile  : xxxxxxxx
Id                : xxxxxxxx
Location          : East US
Name              : ContosoCS
NetworkProfile    : xxxxxxxx
OSProfile         : xxxxxxxx
PackageUrl        : xxxxxxxx
ProvisioningState : Succeeded
RoleProfile       : xxxxxxxx
StartCloudService :
Tag               : {
                      "Owner": "Contos"
                    }
Type              : Microsoft.Compute/cloudServices
UniqueId          : xxxxxxxx
UpgradeMode       : Auto

```

<span data-ttu-id="de586-115">Эта команда получает облачную службу ContosoCS, которая принадлежит к группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="de586-115">This command gets cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="de586-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de586-116">PARAMETERS</span></span>

### <span data-ttu-id="de586-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de586-117">-DefaultProfile</span></span>
<span data-ttu-id="de586-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de586-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de586-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de586-119">-InputObject</span></span>
<span data-ttu-id="de586-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="de586-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de586-121">-Name</span><span class="sxs-lookup"><span data-stu-id="de586-121">-Name</span></span>
<span data-ttu-id="de586-122">Имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="de586-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de586-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de586-123">-ResourceGroupName</span></span>
<span data-ttu-id="de586-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="de586-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de586-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de586-125">-SubscriptionId</span></span>
<span data-ttu-id="de586-126">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="de586-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="de586-127">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="de586-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de586-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de586-128">CommonParameters</span></span>
<span data-ttu-id="de586-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de586-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de586-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de586-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de586-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de586-131">INPUTS</span></span>

### <span data-ttu-id="de586-132">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="de586-132">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="de586-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="de586-133">OUTPUTS</span></span>

### <span data-ttu-id="de586-134">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="de586-134">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="de586-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="de586-135">NOTES</span></span>

<span data-ttu-id="de586-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="de586-136">ALIASES</span></span>

<span data-ttu-id="de586-137">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="de586-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="de586-138">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="de586-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="de586-139">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="de586-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="de586-140">INPUTOBJECT <ICloudServiceIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="de586-140">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="de586-141">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="de586-141">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="de586-142">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="de586-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="de586-143">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="de586-143">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="de586-144">`[RoleInstanceName <String>]`: Имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="de586-144">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="de586-145">`[RoleName <String>]`: название роли.</span><span class="sxs-lookup"><span data-stu-id="de586-145">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="de586-146">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="de586-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="de586-147">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="de586-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="de586-148">`[UpdateDomain <Int32?>]`: Указывает значение, определя которое определяет домен обновления.</span><span class="sxs-lookup"><span data-stu-id="de586-148">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="de586-149">Домены обновления имеют индекс с нулевым индексом: у первого домена обновления — 0, у второго — 1 и так далее.</span><span class="sxs-lookup"><span data-stu-id="de586-149">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="de586-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de586-150">RELATED LINKS</span></span>

