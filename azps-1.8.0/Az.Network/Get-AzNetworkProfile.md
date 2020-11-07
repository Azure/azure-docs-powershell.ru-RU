---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
ms.openlocfilehash: 1f57a8a9cc65ab9ff4955d6d11e6f4c1a91c417e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730539"
---
# <span data-ttu-id="eed9e-101">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eed9e-101">Get-AzNetworkProfile</span></span>

## <span data-ttu-id="eed9e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eed9e-102">SYNOPSIS</span></span>
<span data-ttu-id="eed9e-103">Получает существующий ресурс верхнего уровня профиля сети</span><span class="sxs-lookup"><span data-stu-id="eed9e-103">Gets an existing network profile top level resource</span></span>

## <span data-ttu-id="eed9e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eed9e-104">SYNTAX</span></span>

### <span data-ttu-id="eed9e-105">GetByResourceNameNoExpandParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eed9e-105">GetByResourceNameNoExpandParameterSet (Default)</span></span>
```
Get-AzNetworkProfile [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eed9e-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="eed9e-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eed9e-107">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="eed9e-107">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eed9e-108">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="eed9e-108">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eed9e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eed9e-109">DESCRIPTION</span></span>
<span data-ttu-id="eed9e-110">Командлет **Get-AzNetworkProfile** извлекает существующий ресурс верхнего уровня профиля сети</span><span class="sxs-lookup"><span data-stu-id="eed9e-110">The **Get-AzNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="eed9e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eed9e-111">EXAMPLES</span></span>

### <span data-ttu-id="eed9e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eed9e-112">Example 1</span></span>
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

<span data-ttu-id="eed9e-113">В результате будет извлечен профиль NP1 в группе ресурсов Rg1</span><span class="sxs-lookup"><span data-stu-id="eed9e-113">This retrieves the network profile np1 in resource group rg1</span></span>

### <span data-ttu-id="eed9e-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="eed9e-114">Example 2</span></span>
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

<span data-ttu-id="eed9e-115">Будет извлечены профили сети, которые начинаются с "NP"</span><span class="sxs-lookup"><span data-stu-id="eed9e-115">This retrieves the network profiles that start with "np"</span></span>

## <span data-ttu-id="eed9e-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eed9e-116">PARAMETERS</span></span>

### <span data-ttu-id="eed9e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed9e-117">-DefaultProfile</span></span>
<span data-ttu-id="eed9e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eed9e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eed9e-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="eed9e-119">-ExpandResource</span></span>
<span data-ttu-id="eed9e-120">Развернутая ссылка на ресурс.</span><span class="sxs-lookup"><span data-stu-id="eed9e-120">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="eed9e-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eed9e-121">-Name</span></span>
<span data-ttu-id="eed9e-122">Имя сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="eed9e-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="eed9e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eed9e-123">-ResourceGroupName</span></span>
<span data-ttu-id="eed9e-124">Имя группы ресурсов в сетевом профиле.</span><span class="sxs-lookup"><span data-stu-id="eed9e-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="eed9e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eed9e-125">-ResourceId</span></span>
<span data-ttu-id="eed9e-126">Идентификатор диспетчера ресурсов Azure в сетевом профиле.</span><span class="sxs-lookup"><span data-stu-id="eed9e-126">The Azure resource manager id of the network profile.</span></span>

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

### <span data-ttu-id="eed9e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed9e-127">CommonParameters</span></span>
<span data-ttu-id="eed9e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eed9e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed9e-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eed9e-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed9e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eed9e-130">INPUTS</span></span>

### <span data-ttu-id="eed9e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="eed9e-131">System.String</span></span>

## <span data-ttu-id="eed9e-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eed9e-132">OUTPUTS</span></span>

### <span data-ttu-id="eed9e-133">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eed9e-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="eed9e-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="eed9e-134">NOTES</span></span>

## <span data-ttu-id="eed9e-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eed9e-135">RELATED LINKS</span></span>

[<span data-ttu-id="eed9e-136">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eed9e-136">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="eed9e-137">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eed9e-137">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="eed9e-138">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eed9e-138">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
