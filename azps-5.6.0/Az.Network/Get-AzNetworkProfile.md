---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
ms.openlocfilehash: f2f18ac77f923247f2bef0e78802a2f05cf302d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954536"
---
# <span data-ttu-id="d7efa-101">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d7efa-101">Get-AzNetworkProfile</span></span>

## <span data-ttu-id="d7efa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7efa-102">SYNOPSIS</span></span>
<span data-ttu-id="d7efa-103">Получает существующий ресурс верхнего уровня профиля сети</span><span class="sxs-lookup"><span data-stu-id="d7efa-103">Gets an existing network profile top level resource</span></span>

## <span data-ttu-id="d7efa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d7efa-104">SYNTAX</span></span>

### <span data-ttu-id="d7efa-105">GetByResourceNameNoExpandParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d7efa-105">GetByResourceNameNoExpandParameterSet (Default)</span></span>
```
Get-AzNetworkProfile [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7efa-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7efa-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7efa-107">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7efa-107">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7efa-108">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7efa-108">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7efa-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7efa-109">DESCRIPTION</span></span>
<span data-ttu-id="d7efa-110">Командлет **Get-AzNetworkProfile** извлекает существующий ресурс верхнего уровня профиля сети.</span><span class="sxs-lookup"><span data-stu-id="d7efa-110">The **Get-AzNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="d7efa-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d7efa-111">EXAMPLES</span></span>

### <span data-ttu-id="d7efa-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d7efa-112">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1
```

<span data-ttu-id="d7efa-113">В этом случае будет извлечен профиль сети np1 в группе ресурсов rg1</span><span class="sxs-lookup"><span data-stu-id="d7efa-113">This retrieves the network profile np1 in resource group rg1</span></span>

### <span data-ttu-id="d7efa-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d7efa-114">Example 2</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np*

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np2
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np2
```

<span data-ttu-id="d7efa-115">При этом будут извлекаться профили сети, которые начинаются с "np"</span><span class="sxs-lookup"><span data-stu-id="d7efa-115">This retrieves the network profiles that start with "np"</span></span>

## <span data-ttu-id="d7efa-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7efa-116">PARAMETERS</span></span>

### <span data-ttu-id="d7efa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7efa-117">-DefaultProfile</span></span>
<span data-ttu-id="d7efa-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7efa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7efa-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="d7efa-119">-ExpandResource</span></span>
<span data-ttu-id="d7efa-120">Ссылка на ресурсы, которая должна быть расширена.</span><span class="sxs-lookup"><span data-stu-id="d7efa-120">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceIdExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7efa-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d7efa-121">-Name</span></span>
<span data-ttu-id="d7efa-122">Имя профиля сети.</span><span class="sxs-lookup"><span data-stu-id="d7efa-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d7efa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7efa-123">-ResourceGroupName</span></span>
<span data-ttu-id="d7efa-124">Имя группы ресурсов профиля сети.</span><span class="sxs-lookup"><span data-stu-id="d7efa-124">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d7efa-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7efa-125">-ResourceId</span></span>
<span data-ttu-id="d7efa-126">ИД диспетчера ресурсов Azure в сетевом профиле.</span><span class="sxs-lookup"><span data-stu-id="d7efa-126">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7efa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7efa-127">CommonParameters</span></span>
<span data-ttu-id="d7efa-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7efa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7efa-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7efa-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7efa-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7efa-130">INPUTS</span></span>

### <span data-ttu-id="d7efa-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d7efa-131">System.String</span></span>

## <span data-ttu-id="d7efa-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d7efa-132">OUTPUTS</span></span>

### <span data-ttu-id="d7efa-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d7efa-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="d7efa-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d7efa-134">NOTES</span></span>

## <span data-ttu-id="d7efa-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7efa-135">RELATED LINKS</span></span>

[<span data-ttu-id="d7efa-136">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d7efa-136">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="d7efa-137">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d7efa-137">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="d7efa-138">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d7efa-138">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
