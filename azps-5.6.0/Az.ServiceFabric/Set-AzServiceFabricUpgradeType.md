---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: c117937d674c95f69eb967667c86c503ffbb62c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976323"
---
# <span data-ttu-id="8f2ba-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="8f2ba-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="8f2ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f2ba-102">SYNOPSIS</span></span>
<span data-ttu-id="8f2ba-103">Измените тип обновления "Служивая ткань" для кластера.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="8f2ba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8f2ba-104">SYNTAX</span></span>

### <span data-ttu-id="8f2ba-105">Автоматически</span><span class="sxs-lookup"><span data-stu-id="8f2ba-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f2ba-106">Вручную</span><span class="sxs-lookup"><span data-stu-id="8f2ba-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f2ba-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f2ba-107">DESCRIPTION</span></span>
<span data-ttu-id="8f2ba-108">Используйте **Set-AzServiceFabricUpgradeType,** чтобы установить тип обновления автоматически или вручную с определенной версией кода "Служиная ткань".</span><span class="sxs-lookup"><span data-stu-id="8f2ba-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="8f2ba-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8f2ba-109">EXAMPLES</span></span>

### <span data-ttu-id="8f2ba-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8f2ba-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="8f2ba-111">Эта команда настроит режим обновления кластера на автоматический.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="8f2ba-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f2ba-112">PARAMETERS</span></span>

### <span data-ttu-id="8f2ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f2ba-113">-DefaultProfile</span></span>
<span data-ttu-id="8f2ba-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f2ba-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8f2ba-115">-Name</span></span>
<span data-ttu-id="8f2ba-116">Указание имени кластера</span><span class="sxs-lookup"><span data-stu-id="8f2ba-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="8f2ba-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f2ba-117">-ResourceGroupName</span></span>
<span data-ttu-id="8f2ba-118">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8f2ba-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="8f2ba-119">-UpgradeMode</span></span>
<span data-ttu-id="8f2ba-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="8f2ba-120">ClusterUpgradeMode</span></span>

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

### <span data-ttu-id="8f2ba-121">-Версия</span><span class="sxs-lookup"><span data-stu-id="8f2ba-121">-Version</span></span>
<span data-ttu-id="8f2ba-122">Версия кода кластера</span><span class="sxs-lookup"><span data-stu-id="8f2ba-122">Cluster code version</span></span>

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

### <span data-ttu-id="8f2ba-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f2ba-123">-Confirm</span></span>
<span data-ttu-id="8f2ba-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f2ba-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f2ba-125">-WhatIf</span></span>
<span data-ttu-id="8f2ba-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f2ba-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f2ba-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f2ba-128">CommonParameters</span></span>
<span data-ttu-id="8f2ba-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f2ba-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f2ba-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f2ba-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f2ba-131">INPUTS</span></span>

### <span data-ttu-id="8f2ba-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8f2ba-132">System.String</span></span>

### <span data-ttu-id="8f2ba-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="8f2ba-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="8f2ba-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8f2ba-134">OUTPUTS</span></span>

### <span data-ttu-id="8f2ba-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="8f2ba-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="8f2ba-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8f2ba-136">NOTES</span></span>

## <span data-ttu-id="8f2ba-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f2ba-137">RELATED LINKS</span></span>
