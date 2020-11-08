---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: 3a83b7200f7634574fd457d2fa08f926a62b9a82
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074012"
---
# <span data-ttu-id="8e06c-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8e06c-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="8e06c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e06c-102">SYNOPSIS</span></span>
<span data-ttu-id="8e06c-103">Удаление сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="8e06c-103">Removes a network profile.</span></span>

## <span data-ttu-id="8e06c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e06c-104">SYNTAX</span></span>

### <span data-ttu-id="8e06c-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e06c-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e06c-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e06c-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e06c-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e06c-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e06c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e06c-108">DESCRIPTION</span></span>
<span data-ttu-id="8e06c-109">Командлет **Remove-AzNetworkProfile** удаляет профиль сети, если не были созданы сетевые интерфейсы контейнера (в отличие от **конфигурации** сетевого интерфейса контейнера).</span><span class="sxs-lookup"><span data-stu-id="8e06c-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration** ) have been created.</span></span>

## <span data-ttu-id="8e06c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e06c-110">EXAMPLES</span></span>

### <span data-ttu-id="8e06c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8e06c-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="8e06c-112">Это приведет к удалению сетевого профиля с именем NP1 из группы ресурсов Rg1.</span><span class="sxs-lookup"><span data-stu-id="8e06c-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="8e06c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e06c-113">PARAMETERS</span></span>

### <span data-ttu-id="8e06c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e06c-114">-AsJob</span></span>
<span data-ttu-id="8e06c-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8e06c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e06c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e06c-116">-DefaultProfile</span></span>
<span data-ttu-id="8e06c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e06c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e06c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8e06c-118">-Force</span></span>
<span data-ttu-id="8e06c-119">Не запрашивать подтверждение, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="8e06c-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="8e06c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e06c-120">-InputObject</span></span>
<span data-ttu-id="8e06c-121">Объект профиля сети.</span><span class="sxs-lookup"><span data-stu-id="8e06c-121">Network profile object.</span></span>

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

### <span data-ttu-id="8e06c-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8e06c-122">-Name</span></span>
<span data-ttu-id="8e06c-123">Имя сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="8e06c-123">The name of the network profile.</span></span>

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

### <span data-ttu-id="8e06c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e06c-124">-PassThru</span></span>
<span data-ttu-id="8e06c-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="8e06c-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="8e06c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e06c-126">-ResourceGroupName</span></span>
<span data-ttu-id="8e06c-127">Имя группы ресурсов в сетевом профиле.</span><span class="sxs-lookup"><span data-stu-id="8e06c-127">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="8e06c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e06c-128">-ResourceId</span></span>
<span data-ttu-id="8e06c-129">Идентификатор ресурса диспетчера ресурсов Azure в сетевом профиле.</span><span class="sxs-lookup"><span data-stu-id="8e06c-129">The Azure resource manager resource ID of the network profile.</span></span>

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

### <span data-ttu-id="8e06c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e06c-130">-Confirm</span></span>
<span data-ttu-id="8e06c-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8e06c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e06c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e06c-132">-WhatIf</span></span>
<span data-ttu-id="8e06c-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8e06c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e06c-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8e06c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e06c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e06c-135">CommonParameters</span></span>
<span data-ttu-id="8e06c-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e06c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e06c-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e06c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e06c-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e06c-138">INPUTS</span></span>

### <span data-ttu-id="8e06c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8e06c-139">System.String</span></span>

### <span data-ttu-id="8e06c-140">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8e06c-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="8e06c-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e06c-141">OUTPUTS</span></span>

### <span data-ttu-id="8e06c-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e06c-142">System.Boolean</span></span>

## <span data-ttu-id="8e06c-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e06c-143">NOTES</span></span>

## <span data-ttu-id="8e06c-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e06c-144">RELATED LINKS</span></span>

[<span data-ttu-id="8e06c-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8e06c-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="8e06c-146">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8e06c-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="8e06c-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8e06c-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
