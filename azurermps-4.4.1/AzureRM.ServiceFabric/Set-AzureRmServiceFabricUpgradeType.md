---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
ms.openlocfilehash: 7884e45c2b4f635c9236f213a93eb69524b37fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732405"
---
# <span data-ttu-id="af350-101">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="af350-101">Set-AzureRmServiceFabricUpgradeType</span></span>

## <span data-ttu-id="af350-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af350-102">SYNOPSIS</span></span>
<span data-ttu-id="af350-103">Изменение типа обновления структуры обслуживания кластера.</span><span class="sxs-lookup"><span data-stu-id="af350-103">Change the Service Fabric upgrade type of the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af350-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af350-104">SYNTAX</span></span>

### <span data-ttu-id="af350-105">Автоматически</span><span class="sxs-lookup"><span data-stu-id="af350-105">Automatic</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af350-106">Вручную</span><span class="sxs-lookup"><span data-stu-id="af350-106">Manual</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af350-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af350-107">DESCRIPTION</span></span>
<span data-ttu-id="af350-108">С помощью **Set-AzureRmServiceFabricUpgradeType** настройте тип обновления на автоматически или вручную с определенной версией кода фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="af350-108">Use **Set-AzureRmServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="af350-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af350-109">EXAMPLES</span></span>

### <span data-ttu-id="af350-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="af350-110">Example 1</span></span>
```
PS c:> Set-AzureRmServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="af350-111">Эта команда позволяет настроить режим обновления кластера на автоматический.</span><span class="sxs-lookup"><span data-stu-id="af350-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="af350-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af350-112">PARAMETERS</span></span>

### <span data-ttu-id="af350-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="af350-113">-Name</span></span>
<span data-ttu-id="af350-114">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="af350-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="af350-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af350-115">-ResourceGroupName</span></span>
<span data-ttu-id="af350-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="af350-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="af350-117">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="af350-117">-UpgradeMode</span></span>
<span data-ttu-id="af350-118">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="af350-118">ClusterUpgradeMode</span></span>

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

### <span data-ttu-id="af350-119">-Version</span><span class="sxs-lookup"><span data-stu-id="af350-119">-Version</span></span>
<span data-ttu-id="af350-120">Версия кода кластера.</span><span class="sxs-lookup"><span data-stu-id="af350-120">Cluster code version.</span></span>

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

### <span data-ttu-id="af350-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af350-121">-Confirm</span></span>
<span data-ttu-id="af350-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="af350-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af350-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af350-123">-WhatIf</span></span>
<span data-ttu-id="af350-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="af350-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af350-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="af350-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af350-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af350-126">-DefaultProfile</span></span>
<span data-ttu-id="af350-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af350-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af350-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af350-128">CommonParameters</span></span>
<span data-ttu-id="af350-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af350-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af350-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af350-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af350-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af350-131">INPUTS</span></span>

### <span data-ttu-id="af350-132">Microsoft. Azure. Commands. ServiceFabric. Models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="af350-132">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>
<span data-ttu-id="af350-133">System. String</span><span class="sxs-lookup"><span data-stu-id="af350-133">System.String</span></span>

## <span data-ttu-id="af350-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af350-134">OUTPUTS</span></span>

### <span data-ttu-id="af350-135">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="af350-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="af350-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="af350-136">NOTES</span></span>

## <span data-ttu-id="af350-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af350-137">RELATED LINKS</span></span>

