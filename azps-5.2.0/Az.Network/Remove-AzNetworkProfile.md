---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: 3a83b7200f7634574fd457d2fa08f926a62b9a82
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417036"
---
# <span data-ttu-id="5b1a2-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5b1a2-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="5b1a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b1a2-102">SYNOPSIS</span></span>
<span data-ttu-id="5b1a2-103">Удаляет профиль сети.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-103">Removes a network profile.</span></span>

## <span data-ttu-id="5b1a2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5b1a2-104">SYNTAX</span></span>

### <span data-ttu-id="5b1a2-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5b1a2-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b1a2-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b1a2-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b1a2-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b1a2-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b1a2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b1a2-108">DESCRIPTION</span></span>
<span data-ttu-id="5b1a2-109">Командлет **Remove-AzNetworkProfile** удаляет профиль сети, если не созданы интерфейсы контейнеров (в отличие от конфигурации интерфейса контейнера). </span><span class="sxs-lookup"><span data-stu-id="5b1a2-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration**) have been created.</span></span>

## <span data-ttu-id="5b1a2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5b1a2-110">EXAMPLES</span></span>

### <span data-ttu-id="5b1a2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5b1a2-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="5b1a2-112">При этом профиль сети с именем np1 будет удаляться из группы ресурсов rg1.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="5b1a2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b1a2-113">PARAMETERS</span></span>

### <span data-ttu-id="5b1a2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b1a2-114">-AsJob</span></span>
<span data-ttu-id="5b1a2-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5b1a2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b1a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b1a2-116">-DefaultProfile</span></span>
<span data-ttu-id="5b1a2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b1a2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5b1a2-118">-Force</span></span>
<span data-ttu-id="5b1a2-119">Не спрашивайте подтверждения, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="5b1a2-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="5b1a2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b1a2-120">-InputObject</span></span>
<span data-ttu-id="5b1a2-121">Объект профиля сети.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-121">Network profile object.</span></span>

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

### <span data-ttu-id="5b1a2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5b1a2-122">-Name</span></span>
<span data-ttu-id="5b1a2-123">Имя профиля сети.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-123">The name of the network profile.</span></span>

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

### <span data-ttu-id="5b1a2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b1a2-124">-PassThru</span></span>
<span data-ttu-id="5b1a2-125">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="5b1a2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b1a2-126">-ResourceGroupName</span></span>
<span data-ttu-id="5b1a2-127">Имя группы ресурсов профиля сети.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-127">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="5b1a2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b1a2-128">-ResourceId</span></span>
<span data-ttu-id="5b1a2-129">ИД ресурса диспетчера ресурсов Azure в сетевом профиле.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-129">The Azure resource manager resource ID of the network profile.</span></span>

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

### <span data-ttu-id="5b1a2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b1a2-130">-Confirm</span></span>
<span data-ttu-id="5b1a2-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b1a2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b1a2-132">-WhatIf</span></span>
<span data-ttu-id="5b1a2-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b1a2-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b1a2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b1a2-135">CommonParameters</span></span>
<span data-ttu-id="5b1a2-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b1a2-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b1a2-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b1a2-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b1a2-138">INPUTS</span></span>

### <span data-ttu-id="5b1a2-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5b1a2-139">System.String</span></span>

### <span data-ttu-id="5b1a2-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5b1a2-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="5b1a2-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5b1a2-141">OUTPUTS</span></span>

### <span data-ttu-id="5b1a2-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5b1a2-142">System.Boolean</span></span>

## <span data-ttu-id="5b1a2-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5b1a2-143">NOTES</span></span>

## <span data-ttu-id="5b1a2-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b1a2-144">RELATED LINKS</span></span>

[<span data-ttu-id="5b1a2-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5b1a2-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="5b1a2-146">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5b1a2-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="5b1a2-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5b1a2-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
