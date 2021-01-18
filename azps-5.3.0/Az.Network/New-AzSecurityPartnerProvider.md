---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
ms.openlocfilehash: 5af78bb1f915dec55f75749296340ca6d13a3b3d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518101"
---
# <span data-ttu-id="3cbf6-101">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3cbf6-101">New-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="3cbf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cbf6-102">SYNOPSIS</span></span>
<span data-ttu-id="3cbf6-103">Создает Azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="3cbf6-103">Creates an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="3cbf6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3cbf6-104">SYNTAX</span></span>

```
New-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> -Location <String>
 -SecurityProviderName <String> [-VirtualHub <PSVirtualHub>] [-VirtualHubId <String>]
 [-VirtualHubName <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cbf6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cbf6-105">DESCRIPTION</span></span>
<span data-ttu-id="3cbf6-106">**Новый-AzSecurityPartnerProvider создает** azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="3cbf6-106">The **New-AzSecurityPartnerProvider** cmdlet creates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="3cbf6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3cbf6-107">EXAMPLES</span></span>

### <span data-ttu-id="3cbf6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3cbf6-108">Example 1</span></span>
```powershell
 New-AzSecurityPartnerProvider -Name securityPartnerProviderName -ResourceGroupName rgname -Location 'West US' -SecurityProviderName 'ZScaler'
```

## <span data-ttu-id="3cbf6-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cbf6-109">PARAMETERS</span></span>

### <span data-ttu-id="3cbf6-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cbf6-110">-AsJob</span></span>
<span data-ttu-id="3cbf6-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3cbf6-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cbf6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cbf6-112">-DefaultProfile</span></span>
<span data-ttu-id="3cbf6-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3cbf6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cbf6-114">-Force</span><span class="sxs-lookup"><span data-stu-id="3cbf6-114">-Force</span></span>
<span data-ttu-id="3cbf6-115">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="3cbf6-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cbf6-116">-Location</span><span class="sxs-lookup"><span data-stu-id="3cbf6-116">-Location</span></span>
<span data-ttu-id="3cbf6-117">расположение.</span><span class="sxs-lookup"><span data-stu-id="3cbf6-117">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cbf6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3cbf6-118">-Name</span></span>
<span data-ttu-id="3cbf6-119">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="3cbf6-119">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cbf6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cbf6-120">-ResourceGroupName</span></span>
<span data-ttu-id="3cbf6-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3cbf6-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cbf6-122">-SecurityProviderName</span><span class="sxs-lookup"><span data-stu-id="3cbf6-122">-SecurityProviderName</span></span>
<span data-ttu-id="3cbf6-123">Имя поставщика услуг безопасности</span><span class="sxs-lookup"><span data-stu-id="3cbf6-123">The Security Provider name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ZScaler, IBoss, Checkpoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cbf6-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="3cbf6-124">-Tag</span></span>
<span data-ttu-id="3cbf6-125">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="3cbf6-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cbf6-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="3cbf6-126">-VirtualHub</span></span>
<span data-ttu-id="3cbf6-127">Виртуальный ИД концентратора, к который подключен поставщик услуг безопасности</span><span class="sxs-lookup"><span data-stu-id="3cbf6-127">The virtual hub Id that the security partner provider is attached to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cbf6-128">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="3cbf6-128">-VirtualHubId</span></span>
<span data-ttu-id="3cbf6-129">С ИД VirtualHub этого VpnGateway нужно будет связан.</span><span class="sxs-lookup"><span data-stu-id="3cbf6-129">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cbf6-130">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="3cbf6-130">-VirtualHubName</span></span>
<span data-ttu-id="3cbf6-131">С ИД VirtualHub этого VpnGateway нужно будет связан.</span><span class="sxs-lookup"><span data-stu-id="3cbf6-131">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="3cbf6-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cbf6-132">-Confirm</span></span>
<span data-ttu-id="3cbf6-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cbf6-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cbf6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cbf6-134">-WhatIf</span></span>
<span data-ttu-id="3cbf6-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cbf6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cbf6-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3cbf6-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cbf6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cbf6-137">CommonParameters</span></span>
<span data-ttu-id="3cbf6-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cbf6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cbf6-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cbf6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cbf6-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3cbf6-140">INPUTS</span></span>

### <span data-ttu-id="3cbf6-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3cbf6-141">System.String</span></span>

### <span data-ttu-id="3cbf6-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3cbf6-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="3cbf6-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3cbf6-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3cbf6-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3cbf6-144">OUTPUTS</span></span>

### <span data-ttu-id="3cbf6-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3cbf6-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="3cbf6-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3cbf6-146">NOTES</span></span>

## <span data-ttu-id="3cbf6-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3cbf6-147">RELATED LINKS</span></span>
