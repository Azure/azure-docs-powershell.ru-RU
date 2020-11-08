---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: 346bb9cb073488d0112ea08db22fb1f6c387bac9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243303"
---
# <span data-ttu-id="4965e-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="4965e-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="4965e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4965e-102">SYNOPSIS</span></span>
<span data-ttu-id="4965e-103">Изменение типа обновления структуры обслуживания кластера.</span><span class="sxs-lookup"><span data-stu-id="4965e-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="4965e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4965e-104">SYNTAX</span></span>

### <span data-ttu-id="4965e-105">Автоматически</span><span class="sxs-lookup"><span data-stu-id="4965e-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4965e-106">Вручную</span><span class="sxs-lookup"><span data-stu-id="4965e-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4965e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4965e-107">DESCRIPTION</span></span>
<span data-ttu-id="4965e-108">С помощью **Set-AzServiceFabricUpgradeType** настройте тип обновления на автоматически или вручную с определенной версией кода фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="4965e-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="4965e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4965e-109">EXAMPLES</span></span>

### <span data-ttu-id="4965e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4965e-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="4965e-111">Эта команда позволяет настроить режим обновления кластера на автоматический.</span><span class="sxs-lookup"><span data-stu-id="4965e-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="4965e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4965e-112">PARAMETERS</span></span>

### <span data-ttu-id="4965e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4965e-113">-DefaultProfile</span></span>
<span data-ttu-id="4965e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4965e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4965e-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4965e-115">-Name</span></span>
<span data-ttu-id="4965e-116">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="4965e-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="4965e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4965e-117">-ResourceGroupName</span></span>
<span data-ttu-id="4965e-118">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4965e-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4965e-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="4965e-119">-UpgradeMode</span></span>
<span data-ttu-id="4965e-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="4965e-120">ClusterUpgradeMode</span></span>

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

### <span data-ttu-id="4965e-121">-Version</span><span class="sxs-lookup"><span data-stu-id="4965e-121">-Version</span></span>
<span data-ttu-id="4965e-122">Версия кода кластера</span><span class="sxs-lookup"><span data-stu-id="4965e-122">Cluster code version</span></span>

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

### <span data-ttu-id="4965e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4965e-123">-Confirm</span></span>
<span data-ttu-id="4965e-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4965e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4965e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4965e-125">-WhatIf</span></span>
<span data-ttu-id="4965e-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4965e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4965e-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4965e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4965e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4965e-128">CommonParameters</span></span>
<span data-ttu-id="4965e-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4965e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4965e-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4965e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4965e-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4965e-131">INPUTS</span></span>

### <span data-ttu-id="4965e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4965e-132">System.String</span></span>

### <span data-ttu-id="4965e-133">Microsoft. Azure. Commands. ServiceFabric. Models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="4965e-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="4965e-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4965e-134">OUTPUTS</span></span>

### <span data-ttu-id="4965e-135">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="4965e-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="4965e-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="4965e-136">NOTES</span></span>

## <span data-ttu-id="4965e-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4965e-137">RELATED LINKS</span></span>
