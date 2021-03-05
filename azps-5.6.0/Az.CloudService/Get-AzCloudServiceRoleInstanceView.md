---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
ms.openlocfilehash: 3d3d8e5cd7855e03d5f02ddaee6b38c98aeacb0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008067"
---
# <span data-ttu-id="8d159-101">Get-AzCloudServiceRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="8d159-101">Get-AzCloudServiceRoleInstanceView</span></span>

## <span data-ttu-id="8d159-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d159-102">SYNOPSIS</span></span>
<span data-ttu-id="8d159-103">Извлекает сведения о состоянии времени запуска экземпляра роли в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="8d159-103">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="8d159-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8d159-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8d159-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d159-105">DESCRIPTION</span></span>
<span data-ttu-id="8d159-106">Извлекает сведения о состоянии времени запуска экземпляра роли в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="8d159-106">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="8d159-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8d159-107">EXAMPLES</span></span>

### <span data-ttu-id="8d159-108">Пример 1. Получить сведения о представлении экземпляра для экземпляра роли облачной службы</span><span class="sxs-lookup"><span data-stu-id="8d159-108">Example 1: Get instance view details for cloud service role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Statuses           PlatformFaultDomain PlatformUpdateDomain
--------           ------------------- --------------------
{RoleStateStarted} 0                   0

```

<span data-ttu-id="8d159-109">Этот cmdlet возвращает представление экземпляра роли ContosoFrontEnd_IN_0 облачной службы ContosoCS, которая принадлежит к группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="8d159-109">This cmdlet gets the instance view of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="8d159-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d159-110">PARAMETERS</span></span>

### <span data-ttu-id="8d159-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="8d159-111">-CloudServiceName</span></span>
<span data-ttu-id="8d159-112">.</span><span class="sxs-lookup"><span data-stu-id="8d159-112">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d159-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d159-113">-DefaultProfile</span></span>
<span data-ttu-id="8d159-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d159-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d159-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d159-115">-ResourceGroupName</span></span>
<span data-ttu-id="8d159-116">.</span><span class="sxs-lookup"><span data-stu-id="8d159-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d159-117">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="8d159-117">-RoleInstanceName</span></span>
<span data-ttu-id="8d159-118">Имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="8d159-118">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d159-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d159-119">-SubscriptionId</span></span>
<span data-ttu-id="8d159-120">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8d159-120">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8d159-121">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="8d159-121">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d159-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d159-122">CommonParameters</span></span>
<span data-ttu-id="8d159-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d159-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d159-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d159-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d159-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d159-125">INPUTS</span></span>

## <span data-ttu-id="8d159-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8d159-126">OUTPUTS</span></span>

### <span data-ttu-id="8d159-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="8d159-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span></span>

## <span data-ttu-id="8d159-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8d159-128">NOTES</span></span>

<span data-ttu-id="8d159-129">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8d159-129">ALIASES</span></span>

## <span data-ttu-id="8d159-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d159-130">RELATED LINKS</span></span>

