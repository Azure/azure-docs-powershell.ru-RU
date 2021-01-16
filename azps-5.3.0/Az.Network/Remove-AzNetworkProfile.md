---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: 3a83b7200f7634574fd457d2fa08f926a62b9a82
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506854"
---
# <span data-ttu-id="700ab-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="700ab-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="700ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="700ab-102">SYNOPSIS</span></span>
<span data-ttu-id="700ab-103">Удаляет профиль сети.</span><span class="sxs-lookup"><span data-stu-id="700ab-103">Removes a network profile.</span></span>

## <span data-ttu-id="700ab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="700ab-104">SYNTAX</span></span>

### <span data-ttu-id="700ab-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="700ab-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="700ab-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="700ab-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="700ab-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="700ab-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="700ab-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="700ab-108">DESCRIPTION</span></span>
<span data-ttu-id="700ab-109">Командлет **Remove-AzNetworkProfile** удаляет профиль сети, если не созданы контейнерные сетевые интерфейсы (в отличие от конфигурации интерфейса контейнера). </span><span class="sxs-lookup"><span data-stu-id="700ab-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration**) have been created.</span></span>

## <span data-ttu-id="700ab-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="700ab-110">EXAMPLES</span></span>

### <span data-ttu-id="700ab-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="700ab-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="700ab-112">При этом профиль сети с именем np1 будет удаляться из группы ресурсов rg1.</span><span class="sxs-lookup"><span data-stu-id="700ab-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="700ab-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="700ab-113">PARAMETERS</span></span>

### <span data-ttu-id="700ab-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="700ab-114">-AsJob</span></span>
<span data-ttu-id="700ab-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="700ab-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="700ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="700ab-116">-DefaultProfile</span></span>
<span data-ttu-id="700ab-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="700ab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="700ab-118">-Force</span><span class="sxs-lookup"><span data-stu-id="700ab-118">-Force</span></span>
<span data-ttu-id="700ab-119">Не спрашивайте подтверждения, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="700ab-119">Do not ask for confirmation if you want to delete resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="700ab-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="700ab-120">-InputObject</span></span>
<span data-ttu-id="700ab-121">Объект профиля сети.</span><span class="sxs-lookup"><span data-stu-id="700ab-121">Network profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="700ab-122">-Name</span><span class="sxs-lookup"><span data-stu-id="700ab-122">-Name</span></span>
<span data-ttu-id="700ab-123">Имя профиля сети.</span><span class="sxs-lookup"><span data-stu-id="700ab-123">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="700ab-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="700ab-124">-PassThru</span></span>
<span data-ttu-id="700ab-125">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="700ab-125">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="700ab-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="700ab-126">-ResourceGroupName</span></span>
<span data-ttu-id="700ab-127">Имя группы ресурсов профиля сети.</span><span class="sxs-lookup"><span data-stu-id="700ab-127">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="700ab-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="700ab-128">-ResourceId</span></span>
<span data-ttu-id="700ab-129">ИД ресурса диспетчера ресурсов Azure в профиле сети.</span><span class="sxs-lookup"><span data-stu-id="700ab-129">The Azure resource manager resource ID of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="700ab-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="700ab-130">-Confirm</span></span>
<span data-ttu-id="700ab-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="700ab-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="700ab-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="700ab-132">-WhatIf</span></span>
<span data-ttu-id="700ab-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="700ab-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="700ab-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="700ab-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="700ab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="700ab-135">CommonParameters</span></span>
<span data-ttu-id="700ab-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="700ab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="700ab-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="700ab-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="700ab-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="700ab-138">INPUTS</span></span>

### <span data-ttu-id="700ab-139">System.String</span><span class="sxs-lookup"><span data-stu-id="700ab-139">System.String</span></span>

### <span data-ttu-id="700ab-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="700ab-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="700ab-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="700ab-141">OUTPUTS</span></span>

### <span data-ttu-id="700ab-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="700ab-142">System.Boolean</span></span>

## <span data-ttu-id="700ab-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="700ab-143">NOTES</span></span>

## <span data-ttu-id="700ab-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="700ab-144">RELATED LINKS</span></span>

[<span data-ttu-id="700ab-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="700ab-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="700ab-146">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="700ab-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="700ab-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="700ab-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)