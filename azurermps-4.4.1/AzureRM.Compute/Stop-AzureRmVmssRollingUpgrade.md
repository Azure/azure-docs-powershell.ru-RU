---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: f87399901e00e19686d879799dbb799c7d79172c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569603"
---
# <span data-ttu-id="40d83-101">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="40d83-101">Stop-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="40d83-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40d83-102">SYNOPSIS</span></span>
<span data-ttu-id="40d83-103">Отменяет текущую виртуальную машину с установленным параметром чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="40d83-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40d83-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40d83-104">SYNTAX</span></span>

### <span data-ttu-id="40d83-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="40d83-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40d83-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="40d83-106">FriendMethod</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40d83-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40d83-107">DESCRIPTION</span></span>
<span data-ttu-id="40d83-108">Отменяет текущую виртуальную машину с установленным параметром чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="40d83-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="40d83-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40d83-109">EXAMPLES</span></span>

### <span data-ttu-id="40d83-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="40d83-110">Example 1</span></span>
```
PS C:\> Stop-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="40d83-111">Эта команда отменяет переход на новую версию шкалы виртуальных машин "VMSS001" в группе ресурсов "Group001".</span><span class="sxs-lookup"><span data-stu-id="40d83-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="40d83-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40d83-112">PARAMETERS</span></span>

### <span data-ttu-id="40d83-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d83-113">-DefaultProfile</span></span>
<span data-ttu-id="40d83-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40d83-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40d83-115">-Force</span><span class="sxs-lookup"><span data-stu-id="40d83-115">-Force</span></span>
<span data-ttu-id="40d83-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="40d83-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="40d83-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40d83-117">-ResourceGroupName</span></span>
<span data-ttu-id="40d83-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="40d83-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d83-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="40d83-119">-VMScaleSetName</span></span>
<span data-ttu-id="40d83-120">Имя набора масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="40d83-120">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d83-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40d83-121">-Confirm</span></span>
<span data-ttu-id="40d83-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="40d83-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40d83-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40d83-123">-WhatIf</span></span>
<span data-ttu-id="40d83-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="40d83-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40d83-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="40d83-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40d83-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d83-126">CommonParameters</span></span>
<span data-ttu-id="40d83-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40d83-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d83-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40d83-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d83-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40d83-129">INPUTS</span></span>

### <span data-ttu-id="40d83-130">System. String</span><span class="sxs-lookup"><span data-stu-id="40d83-130">System.String</span></span>

## <span data-ttu-id="40d83-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40d83-131">OUTPUTS</span></span>

### <span data-ttu-id="40d83-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="40d83-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="40d83-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="40d83-133">NOTES</span></span>

## <span data-ttu-id="40d83-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40d83-134">RELATED LINKS</span></span>

