---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkProfile.md
ms.openlocfilehash: ebf2a58530f1dabe0e320dd78a38c63c86565c73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734336"
---
# <span data-ttu-id="e9b19-101">Remove-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e9b19-101">Remove-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="e9b19-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e9b19-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b19-103">Удаление сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="e9b19-103">Removes a network profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9b19-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e9b19-104">SYNTAX</span></span>

### <span data-ttu-id="e9b19-105">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="e9b19-105">RemoveByName</span></span>
```
Remove-AzureRmNetworkProfile -ResourceGroupName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9b19-106">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9b19-106">RemoveByNameParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9b19-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9b19-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9b19-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9b19-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9b19-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9b19-109">DESCRIPTION</span></span>
<span data-ttu-id="e9b19-110">Командлет **Remove-AzureRmNetworkProfile** удаляет профиль сети, если не были созданы сетевые интерфейсы контейнера (в отличие от **конфигурации** сетевого интерфейса контейнера).</span><span class="sxs-lookup"><span data-stu-id="e9b19-110">The **Remove-AzureRmNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration** ) have been created.</span></span>

## <span data-ttu-id="e9b19-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e9b19-111">EXAMPLES</span></span>

### <span data-ttu-id="e9b19-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e9b19-112">Example 1</span></span>
```powershell
Remove-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="e9b19-113">Это приведет к удалению сетевого профиля с именем NP1 из группы ресурсов Rg1.</span><span class="sxs-lookup"><span data-stu-id="e9b19-113">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="e9b19-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e9b19-114">PARAMETERS</span></span>

### <span data-ttu-id="e9b19-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9b19-115">-AsJob</span></span>
<span data-ttu-id="e9b19-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e9b19-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9b19-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b19-117">-DefaultProfile</span></span>
<span data-ttu-id="e9b19-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9b19-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b19-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e9b19-119">-Force</span></span>
<span data-ttu-id="e9b19-120">Не запрашивать подтверждение, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="e9b19-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="e9b19-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9b19-121">-InputObject</span></span>
<span data-ttu-id="e9b19-122">Объект профиля сети.</span><span class="sxs-lookup"><span data-stu-id="e9b19-122">Network profile object.</span></span>

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

### <span data-ttu-id="e9b19-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e9b19-123">-Name</span></span>
<span data-ttu-id="e9b19-124">Имя сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="e9b19-124">The name of the network profile.</span></span>

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

### <span data-ttu-id="e9b19-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9b19-125">-PassThru</span></span>
<span data-ttu-id="e9b19-126">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="e9b19-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e9b19-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9b19-127">-ResourceGroupName</span></span>
<span data-ttu-id="e9b19-128">Имя группы ресурсов в сетевом профиле.</span><span class="sxs-lookup"><span data-stu-id="e9b19-128">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="e9b19-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9b19-129">-ResourceId</span></span>
<span data-ttu-id="e9b19-130">Идентификатор ресурса диспетчера ресурсов Azure в сетевом профиле.</span><span class="sxs-lookup"><span data-stu-id="e9b19-130">The Azure resource manager resource ID of the network profile.</span></span>

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

### <span data-ttu-id="e9b19-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9b19-131">-Confirm</span></span>
<span data-ttu-id="e9b19-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e9b19-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9b19-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9b19-133">-WhatIf</span></span>
<span data-ttu-id="e9b19-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e9b19-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9b19-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e9b19-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9b19-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b19-136">CommonParameters</span></span>
<span data-ttu-id="e9b19-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e9b19-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b19-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9b19-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b19-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e9b19-139">INPUTS</span></span>

### <span data-ttu-id="e9b19-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e9b19-140">System.String</span></span>

## <span data-ttu-id="e9b19-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9b19-141">OUTPUTS</span></span>

### <span data-ttu-id="e9b19-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e9b19-142">System.Boolean</span></span>

## <span data-ttu-id="e9b19-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="e9b19-143">NOTES</span></span>

## <span data-ttu-id="e9b19-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9b19-144">RELATED LINKS</span></span>
