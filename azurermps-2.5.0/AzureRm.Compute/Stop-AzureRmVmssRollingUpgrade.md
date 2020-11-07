---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmssrollingupgrade
schema: 2.0.0
ms.openlocfilehash: 8893f5fc8f6bf798635fdfd5e9a16bc4179815e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915354"
---
# <span data-ttu-id="14f61-101">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="14f61-101">Stop-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="14f61-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14f61-102">SYNOPSIS</span></span>
<span data-ttu-id="14f61-103">Отменяет текущую виртуальную машину с установленным параметром чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="14f61-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14f61-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14f61-104">SYNTAX</span></span>

### <span data-ttu-id="14f61-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="14f61-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14f61-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="14f61-106">FriendMethod</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14f61-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14f61-107">DESCRIPTION</span></span>
<span data-ttu-id="14f61-108">Отменяет текущую виртуальную машину с установленным параметром чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="14f61-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="14f61-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14f61-109">EXAMPLES</span></span>

### <span data-ttu-id="14f61-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="14f61-110">Example 1</span></span>
```
PS C:\> Stop-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="14f61-111">Эта команда отменяет переход на новую версию шкалы виртуальных машин "VMSS001" в группе ресурсов "Group001".</span><span class="sxs-lookup"><span data-stu-id="14f61-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="14f61-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14f61-112">PARAMETERS</span></span>

### <span data-ttu-id="14f61-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14f61-113">-AsJob</span></span>
<span data-ttu-id="14f61-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="14f61-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14f61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f61-115">-DefaultProfile</span></span>
<span data-ttu-id="14f61-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14f61-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14f61-117">-Force</span><span class="sxs-lookup"><span data-stu-id="14f61-117">-Force</span></span>
<span data-ttu-id="14f61-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="14f61-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="14f61-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14f61-119">-ResourceGroupName</span></span>
<span data-ttu-id="14f61-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="14f61-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14f61-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="14f61-121">-VMScaleSetName</span></span>
<span data-ttu-id="14f61-122">Имя набора масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="14f61-122">The name of the VM scale set.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14f61-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14f61-123">-Confirm</span></span>
<span data-ttu-id="14f61-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="14f61-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14f61-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14f61-125">-WhatIf</span></span>
<span data-ttu-id="14f61-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="14f61-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14f61-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="14f61-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14f61-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f61-128">CommonParameters</span></span>
<span data-ttu-id="14f61-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14f61-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f61-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14f61-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f61-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14f61-131">INPUTS</span></span>

### <span data-ttu-id="14f61-132">System. String</span><span class="sxs-lookup"><span data-stu-id="14f61-132">System.String</span></span>

## <span data-ttu-id="14f61-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14f61-133">OUTPUTS</span></span>

### <span data-ttu-id="14f61-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="14f61-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="14f61-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="14f61-135">NOTES</span></span>

## <span data-ttu-id="14f61-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14f61-136">RELATED LINKS</span></span>

