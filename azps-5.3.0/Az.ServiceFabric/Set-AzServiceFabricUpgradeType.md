---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: 346bb9cb073488d0112ea08db22fb1f6c387bac9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517177"
---
# <span data-ttu-id="8ee33-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="8ee33-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="8ee33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ee33-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee33-103">Измените тип обновления "Служивная ткань" для кластера.</span><span class="sxs-lookup"><span data-stu-id="8ee33-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="8ee33-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8ee33-104">SYNTAX</span></span>

### <span data-ttu-id="8ee33-105">Автоматически</span><span class="sxs-lookup"><span data-stu-id="8ee33-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ee33-106">Вручную</span><span class="sxs-lookup"><span data-stu-id="8ee33-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ee33-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ee33-107">DESCRIPTION</span></span>
<span data-ttu-id="8ee33-108">Используйте **Set-AzServiceFabricUpgradeType,** чтобы установить тип обновления автоматически или вручную с определенной версией кода "Служиная ткань".</span><span class="sxs-lookup"><span data-stu-id="8ee33-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="8ee33-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8ee33-109">EXAMPLES</span></span>

### <span data-ttu-id="8ee33-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8ee33-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="8ee33-111">Эта команда настроит режим обновления кластера на автоматический.</span><span class="sxs-lookup"><span data-stu-id="8ee33-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="8ee33-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ee33-112">PARAMETERS</span></span>

### <span data-ttu-id="8ee33-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ee33-113">-DefaultProfile</span></span>
<span data-ttu-id="8ee33-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ee33-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ee33-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8ee33-115">-Name</span></span>
<span data-ttu-id="8ee33-116">Указание имени кластера</span><span class="sxs-lookup"><span data-stu-id="8ee33-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ee33-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ee33-117">-ResourceGroupName</span></span>
<span data-ttu-id="8ee33-118">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ee33-118">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ee33-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="8ee33-119">-UpgradeMode</span></span>
<span data-ttu-id="8ee33-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="8ee33-120">ClusterUpgradeMode</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ee33-121">-Version</span><span class="sxs-lookup"><span data-stu-id="8ee33-121">-Version</span></span>
<span data-ttu-id="8ee33-122">Версия кода кластера</span><span class="sxs-lookup"><span data-stu-id="8ee33-122">Cluster code version</span></span>

```yaml
Type: System.String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ee33-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ee33-123">-Confirm</span></span>
<span data-ttu-id="8ee33-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ee33-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ee33-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ee33-125">-WhatIf</span></span>
<span data-ttu-id="8ee33-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ee33-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ee33-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8ee33-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ee33-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee33-128">CommonParameters</span></span>
<span data-ttu-id="8ee33-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ee33-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee33-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ee33-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee33-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ee33-131">INPUTS</span></span>

### <span data-ttu-id="8ee33-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8ee33-132">System.String</span></span>

### <span data-ttu-id="8ee33-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="8ee33-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="8ee33-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8ee33-134">OUTPUTS</span></span>

### <span data-ttu-id="8ee33-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="8ee33-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="8ee33-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8ee33-136">NOTES</span></span>

## <span data-ttu-id="8ee33-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ee33-137">RELATED LINKS</span></span>
