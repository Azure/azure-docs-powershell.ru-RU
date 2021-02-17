---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
ms.openlocfilehash: a86ebbda321f37a38b3d014377081087f37feb9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215860"
---
# <span data-ttu-id="6448d-101">Get-AzCloudServiceRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="6448d-101">Get-AzCloudServiceRoleInstanceView</span></span>

## <span data-ttu-id="6448d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6448d-102">SYNOPSIS</span></span>
<span data-ttu-id="6448d-103">Извлекает сведения о состоянии времени запуска экземпляра роли в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="6448d-103">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="6448d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6448d-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6448d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6448d-105">DESCRIPTION</span></span>
<span data-ttu-id="6448d-106">Извлекает сведения о состоянии времени запуска экземпляра роли в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="6448d-106">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="6448d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6448d-107">EXAMPLES</span></span>

### <span data-ttu-id="6448d-108">Пример 1. Получить сведения о представлении экземпляра для экземпляра роли облачной службы</span><span class="sxs-lookup"><span data-stu-id="6448d-108">Example 1: Get instance view details for cloud service role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Statuses           PlatformFaultDomain PlatformUpdateDomain
--------           ------------------- --------------------
{RoleStateStarted} 0                   0

```

<span data-ttu-id="6448d-109">Этот cmdlet возвращает представление экземпляра роли ContosoFrontEnd_IN_0 облачной службы ContosoCS, которая принадлежит к группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="6448d-109">This cmdlet gets the instance view of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="6448d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6448d-110">PARAMETERS</span></span>

### <span data-ttu-id="6448d-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="6448d-111">-CloudServiceName</span></span>
<span data-ttu-id="6448d-112">.</span><span class="sxs-lookup"><span data-stu-id="6448d-112">.</span></span>

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

### <span data-ttu-id="6448d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6448d-113">-DefaultProfile</span></span>
<span data-ttu-id="6448d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6448d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6448d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6448d-115">-ResourceGroupName</span></span>
<span data-ttu-id="6448d-116">.</span><span class="sxs-lookup"><span data-stu-id="6448d-116">.</span></span>

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

### <span data-ttu-id="6448d-117">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="6448d-117">-RoleInstanceName</span></span>
<span data-ttu-id="6448d-118">Имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="6448d-118">Name of the role instance.</span></span>

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

### <span data-ttu-id="6448d-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6448d-119">-SubscriptionId</span></span>
<span data-ttu-id="6448d-120">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6448d-120">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6448d-121">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="6448d-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6448d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6448d-122">CommonParameters</span></span>
<span data-ttu-id="6448d-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6448d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6448d-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6448d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6448d-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6448d-125">INPUTS</span></span>

## <span data-ttu-id="6448d-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6448d-126">OUTPUTS</span></span>

### <span data-ttu-id="6448d-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="6448d-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span></span>

## <span data-ttu-id="6448d-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6448d-128">NOTES</span></span>

<span data-ttu-id="6448d-129">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6448d-129">ALIASES</span></span>

## <span data-ttu-id="6448d-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6448d-130">RELATED LINKS</span></span>

