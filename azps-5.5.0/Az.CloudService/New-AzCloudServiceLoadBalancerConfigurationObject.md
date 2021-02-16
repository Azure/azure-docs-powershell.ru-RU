---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
ms.openlocfilehash: 6afabb94ae006cec122d7e89997be17c20e85b05
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233497"
---
# <span data-ttu-id="2bf32-101">New-AzCloudServiceLoadBalancerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="2bf32-101">New-AzCloudServiceLoadBalancerConfigurationObject</span></span>

## <span data-ttu-id="2bf32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bf32-102">SYNOPSIS</span></span>
<span data-ttu-id="2bf32-103">Создание в памяти объекта для LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bf32-103">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="2bf32-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2bf32-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerConfigurationObject
 [-FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>] [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="2bf32-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2bf32-105">DESCRIPTION</span></span>
<span data-ttu-id="2bf32-106">Создание в памяти объекта для LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bf32-106">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="2bf32-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2bf32-107">EXAMPLES</span></span>

### <span data-ttu-id="2bf32-108">Пример 1. Создание объекта конфигурации балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="2bf32-108">Example 1: Create load balancer configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIP.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="2bf32-109">Эта команда создает объект конфигурации балансиров нагрузки, который используется для создания или обновления облачной службы.</span><span class="sxs-lookup"><span data-stu-id="2bf32-109">This command creates load balancer configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="2bf32-110">Дополнительные сведения см. в службе New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="2bf32-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="2bf32-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2bf32-111">PARAMETERS</span></span>

### <span data-ttu-id="2bf32-112">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bf32-112">-FrontendIPConfiguration</span></span>
<span data-ttu-id="2bf32-113">FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2bf32-113">FrontendIPConfiguration.</span></span>
<span data-ttu-id="2bf32-114">Чтобы создать новую таблицу, см. раздел "ЗАМЕТКИ" для свойств FRONTENDIPCONFIGURATION и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="2bf32-114">To construct, see NOTES section for FRONTENDIPCONFIGURATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ILoadBalancerFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf32-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2bf32-115">-Name</span></span>
<span data-ttu-id="2bf32-116">Имя LoadBalancerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2bf32-116">Name of LoadBalancerConfiguration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf32-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bf32-117">CommonParameters</span></span>
<span data-ttu-id="2bf32-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bf32-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bf32-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2bf32-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bf32-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2bf32-120">INPUTS</span></span>

## <span data-ttu-id="2bf32-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2bf32-121">OUTPUTS</span></span>

### <span data-ttu-id="2bf32-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bf32-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span></span>

## <span data-ttu-id="2bf32-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2bf32-123">NOTES</span></span>

<span data-ttu-id="2bf32-124">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2bf32-124">ALIASES</span></span>

<span data-ttu-id="2bf32-125">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="2bf32-125">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2bf32-126">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="2bf32-126">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2bf32-127">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2bf32-127">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2bf32-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2bf32-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span></span>
  - <span data-ttu-id="2bf32-129">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="2bf32-129">`[Name <String>]`:</span></span> 
  - <span data-ttu-id="2bf32-130">`[PrivateIPAddress <String>]`: личный IP-адрес, на который ссылается облачная служба.</span><span class="sxs-lookup"><span data-stu-id="2bf32-130">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
  - <span data-ttu-id="2bf32-131">`[PublicIPAddressId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="2bf32-131">`[PublicIPAddressId <String>]`: Resource Id</span></span>
  - <span data-ttu-id="2bf32-132">`[SubnetId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="2bf32-132">`[SubnetId <String>]`: Resource Id</span></span>

## <span data-ttu-id="2bf32-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2bf32-133">RELATED LINKS</span></span>

