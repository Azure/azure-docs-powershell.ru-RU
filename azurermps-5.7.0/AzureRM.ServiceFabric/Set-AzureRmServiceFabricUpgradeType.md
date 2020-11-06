---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
ms.openlocfilehash: 8a675355806a8b4579abcea965a5e0e0b8128207
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567911"
---
# <span data-ttu-id="75e23-101">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="75e23-101">Set-AzureRmServiceFabricUpgradeType</span></span>

## <span data-ttu-id="75e23-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75e23-102">SYNOPSIS</span></span>
<span data-ttu-id="75e23-103">Изменение типа обновления структуры обслуживания кластера.</span><span class="sxs-lookup"><span data-stu-id="75e23-103">Change the Service Fabric upgrade type of the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75e23-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75e23-104">SYNTAX</span></span>

### <span data-ttu-id="75e23-105">Автоматически</span><span class="sxs-lookup"><span data-stu-id="75e23-105">Automatic</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75e23-106">Вручную</span><span class="sxs-lookup"><span data-stu-id="75e23-106">Manual</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75e23-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75e23-107">DESCRIPTION</span></span>
<span data-ttu-id="75e23-108">С помощью **Set-AzureRmServiceFabricUpgradeType** настройте тип обновления на автоматически или вручную с определенной версией кода фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="75e23-108">Use **Set-AzureRmServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="75e23-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75e23-109">EXAMPLES</span></span>

### <span data-ttu-id="75e23-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75e23-110">Example 1</span></span>
```
PS c:> Set-AzureRmServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="75e23-111">Эта команда позволяет настроить режим обновления кластера на автоматический.</span><span class="sxs-lookup"><span data-stu-id="75e23-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="75e23-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75e23-112">PARAMETERS</span></span>

### <span data-ttu-id="75e23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75e23-113">-DefaultProfile</span></span>
<span data-ttu-id="75e23-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75e23-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75e23-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="75e23-115">-Name</span></span>
<span data-ttu-id="75e23-116">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="75e23-116">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75e23-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75e23-117">-ResourceGroupName</span></span>
<span data-ttu-id="75e23-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75e23-118">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75e23-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="75e23-119">-UpgradeMode</span></span>
<span data-ttu-id="75e23-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="75e23-120">ClusterUpgradeMode</span></span>

```yaml
Type: ClusterUpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75e23-121">-Version</span><span class="sxs-lookup"><span data-stu-id="75e23-121">-Version</span></span>
<span data-ttu-id="75e23-122">Версия кода кластера.</span><span class="sxs-lookup"><span data-stu-id="75e23-122">Cluster code version.</span></span>

```yaml
Type: String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75e23-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75e23-123">-Confirm</span></span>
<span data-ttu-id="75e23-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="75e23-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75e23-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75e23-125">-WhatIf</span></span>
<span data-ttu-id="75e23-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="75e23-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75e23-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="75e23-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75e23-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75e23-128">CommonParameters</span></span>
<span data-ttu-id="75e23-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75e23-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75e23-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75e23-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75e23-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75e23-131">INPUTS</span></span>

### <span data-ttu-id="75e23-132">Microsoft. Azure. Commands. ServiceFabric. Models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="75e23-132">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>
<span data-ttu-id="75e23-133">System. String</span><span class="sxs-lookup"><span data-stu-id="75e23-133">System.String</span></span>

## <span data-ttu-id="75e23-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75e23-134">OUTPUTS</span></span>

### <span data-ttu-id="75e23-135">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="75e23-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="75e23-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="75e23-136">NOTES</span></span>

## <span data-ttu-id="75e23-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75e23-137">RELATED LINKS</span></span>

