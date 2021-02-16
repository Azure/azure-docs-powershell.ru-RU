---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerFrontendIPConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
ms.openlocfilehash: cdd983e2ede5cd06c3b9b00805b337eac5b73a9b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229193"
---
# <span data-ttu-id="b1ac9-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="b1ac9-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span></span>

## <span data-ttu-id="b1ac9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="b1ac9-103">Создание в памяти объекта для LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1ac9-103">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="b1ac9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b1ac9-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject [-Name <String>] [-PublicIPAddressId <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1ac9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1ac9-105">DESCRIPTION</span></span>
<span data-ttu-id="b1ac9-106">Создание в памяти объекта для LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1ac9-106">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="b1ac9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b1ac9-107">EXAMPLES</span></span>

### <span data-ttu-id="b1ac9-108">Пример 1. Создание объекта конфигурации переднего IP-адреса балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="b1ac9-108">Example 1: Create load balancer frontend IP configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="b1ac9-109">Эта команда создает объект конфигурации ПЕРЕДНЕГО IP-адреса балансира нагрузки, который используется для создания или обновления облачной службы.</span><span class="sxs-lookup"><span data-stu-id="b1ac9-109">This command creates load balancer frontend IP configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="b1ac9-110">Дополнительные сведения см. в службе New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="b1ac9-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="b1ac9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1ac9-111">PARAMETERS</span></span>

### <span data-ttu-id="b1ac9-112">-Name</span><span class="sxs-lookup"><span data-stu-id="b1ac9-112">-Name</span></span>
<span data-ttu-id="b1ac9-113">Имя FrontendIpConfigration.</span><span class="sxs-lookup"><span data-stu-id="b1ac9-113">Name of FrontendIpConfigration.</span></span>

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

### <span data-ttu-id="b1ac9-114">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="b1ac9-114">-PublicIPAddressId</span></span>
<span data-ttu-id="b1ac9-115">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="b1ac9-115">Resource Id.</span></span>

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

### <span data-ttu-id="b1ac9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1ac9-116">CommonParameters</span></span>
<span data-ttu-id="b1ac9-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1ac9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1ac9-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1ac9-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1ac9-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1ac9-119">INPUTS</span></span>

## <span data-ttu-id="b1ac9-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b1ac9-120">OUTPUTS</span></span>

### <span data-ttu-id="b1ac9-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1ac9-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="b1ac9-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b1ac9-122">NOTES</span></span>

<span data-ttu-id="b1ac9-123">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b1ac9-123">ALIASES</span></span>

## <span data-ttu-id="b1ac9-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1ac9-124">RELATED LINKS</span></span>

