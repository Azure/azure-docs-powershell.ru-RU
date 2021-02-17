---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 55416adbd2ffbcb816e5652ad33e1777594fdcb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215868"
---
# <span data-ttu-id="a5e20-101">Get-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="a5e20-101">Get-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="a5e20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5e20-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e20-103">Получает экземпляр роли из облачной службы.</span><span class="sxs-lookup"><span data-stu-id="a5e20-103">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="a5e20-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a5e20-104">SYNTAX</span></span>

### <span data-ttu-id="a5e20-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5e20-105">List (Default)</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a5e20-106">Получить</span><span class="sxs-lookup"><span data-stu-id="a5e20-106">Get</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a5e20-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a5e20-107">GetViaIdentity</span></span>
```
Get-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a5e20-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5e20-108">DESCRIPTION</span></span>
<span data-ttu-id="a5e20-109">Получает экземпляр роли из облачной службы.</span><span class="sxs-lookup"><span data-stu-id="a5e20-109">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="a5e20-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a5e20-110">EXAMPLES</span></span>

### <span data-ttu-id="a5e20-111">Пример 1. Получить все экземпляры ролей</span><span class="sxs-lookup"><span data-stu-id="a5e20-111">Example 1: Get all role instances</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard
ContosoFrontEnd_IN_1    eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="a5e20-112">Эта команда получает свойства всех экземпляров роли облачной службы ContosoCS, которые принадлежат группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="a5e20-112">This command gets the properties of all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="a5e20-113">Пример 2. Получить свойства для одного экземпляра роли</span><span class="sxs-lookup"><span data-stu-id="a5e20-113">Example 2: Get properties for single role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="a5e20-114">Эта команда получает свойства экземпляра роли ContosoFrontEnd_IN_0 облачной службы ContosoCS, которая принадлежит к группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="a5e20-114">This command gets the properties of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="a5e20-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5e20-115">PARAMETERS</span></span>

### <span data-ttu-id="a5e20-116">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="a5e20-116">-CloudServiceName</span></span>
<span data-ttu-id="a5e20-117">.</span><span class="sxs-lookup"><span data-stu-id="a5e20-117">.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e20-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e20-118">-DefaultProfile</span></span>
<span data-ttu-id="a5e20-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5e20-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5e20-120">-Развернуть</span><span class="sxs-lookup"><span data-stu-id="a5e20-120">-Expand</span></span>
<span data-ttu-id="a5e20-121">Выражение для расширения, применяемая к операции.</span><span class="sxs-lookup"><span data-stu-id="a5e20-121">The expand expression to apply to the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.InstanceViewTypes
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e20-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5e20-122">-InputObject</span></span>
<span data-ttu-id="a5e20-123">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="a5e20-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a5e20-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5e20-124">-ResourceGroupName</span></span>
<span data-ttu-id="a5e20-125">.</span><span class="sxs-lookup"><span data-stu-id="a5e20-125">.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e20-126">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="a5e20-126">-RoleInstanceName</span></span>
<span data-ttu-id="a5e20-127">Имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="a5e20-127">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e20-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5e20-128">-SubscriptionId</span></span>
<span data-ttu-id="a5e20-129">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a5e20-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a5e20-130">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="a5e20-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e20-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e20-131">CommonParameters</span></span>
<span data-ttu-id="a5e20-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5e20-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e20-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5e20-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e20-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5e20-134">INPUTS</span></span>

### <span data-ttu-id="a5e20-135">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="a5e20-135">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="a5e20-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a5e20-136">OUTPUTS</span></span>

### <span data-ttu-id="a5e20-137">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstance</span><span class="sxs-lookup"><span data-stu-id="a5e20-137">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstance</span></span>

## <span data-ttu-id="a5e20-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a5e20-138">NOTES</span></span>

<span data-ttu-id="a5e20-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a5e20-139">ALIASES</span></span>

<span data-ttu-id="a5e20-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a5e20-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a5e20-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="a5e20-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a5e20-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a5e20-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a5e20-143">INPUTOBJECT <ICloudServiceIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="a5e20-143">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a5e20-144">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="a5e20-144">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="a5e20-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="a5e20-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a5e20-146">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="a5e20-146">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="a5e20-147">`[RoleInstanceName <String>]`: имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="a5e20-147">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="a5e20-148">`[RoleName <String>]`: название роли.</span><span class="sxs-lookup"><span data-stu-id="a5e20-148">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="a5e20-149">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a5e20-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a5e20-150">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="a5e20-150">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a5e20-151">`[UpdateDomain <Int32?>]`: Указывает значение, определя которое определяет домен обновления.</span><span class="sxs-lookup"><span data-stu-id="a5e20-151">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="a5e20-152">Домены обновления имеют индекс с нулевым индексом: у первого домена обновления — 0, у второго — 1 и так далее.</span><span class="sxs-lookup"><span data-stu-id="a5e20-152">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="a5e20-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5e20-153">RELATED LINKS</span></span>

