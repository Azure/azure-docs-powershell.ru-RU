---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
ms.openlocfilehash: e02bc88b8f8a3436270f48aea6d9d316dab79318
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734466"
---
# <span data-ttu-id="eaa96-101">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="eaa96-101">Start-AzureRmVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="eaa96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eaa96-102">SYNOPSIS</span></span>
<span data-ttu-id="eaa96-103">Запускает чередующееся обновление, чтобы переместить все экземпляры наборов масштабов виртуальных машин в последнюю доступную версию ОС образа платформы.</span><span class="sxs-lookup"><span data-stu-id="eaa96-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaa96-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eaa96-104">SYNTAX</span></span>

```
Start-AzureRmVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaa96-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eaa96-105">DESCRIPTION</span></span>
<span data-ttu-id="eaa96-106">Запускает чередующееся обновление, чтобы переместить все экземпляры наборов масштабов виртуальных машин в последнюю доступную версию ОС образа платформы.</span><span class="sxs-lookup"><span data-stu-id="eaa96-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="eaa96-107">Для экземпляров, уже использующих последнюю доступную версию операционной системы, это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="eaa96-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="eaa96-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eaa96-108">EXAMPLES</span></span>

### <span data-ttu-id="eaa96-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eaa96-109">Example 1</span></span>
```
PS C:\> Start-AzureRmVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="eaa96-110">Эта команда запускает чередующееся обновление всех экземпляров виртуальной машины, установленной на "VMSS001" в группе ресурсов "Group001".</span><span class="sxs-lookup"><span data-stu-id="eaa96-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="eaa96-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eaa96-111">PARAMETERS</span></span>

### <span data-ttu-id="eaa96-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eaa96-112">-AsJob</span></span>
<span data-ttu-id="eaa96-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="eaa96-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eaa96-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaa96-114">-DefaultProfile</span></span>
<span data-ttu-id="eaa96-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eaa96-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaa96-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaa96-116">-ResourceGroupName</span></span>
<span data-ttu-id="eaa96-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eaa96-117">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaa96-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="eaa96-118">-VMScaleSetName</span></span>
<span data-ttu-id="eaa96-119">Имя набора масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="eaa96-119">The name of the VM scale set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaa96-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eaa96-120">-Confirm</span></span>
<span data-ttu-id="eaa96-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eaa96-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaa96-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaa96-122">-WhatIf</span></span>
<span data-ttu-id="eaa96-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eaa96-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaa96-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eaa96-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaa96-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaa96-125">CommonParameters</span></span>
<span data-ttu-id="eaa96-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eaa96-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaa96-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaa96-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaa96-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eaa96-128">INPUTS</span></span>

### <span data-ttu-id="eaa96-129">System. String</span><span class="sxs-lookup"><span data-stu-id="eaa96-129">System.String</span></span>

## <span data-ttu-id="eaa96-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eaa96-130">OUTPUTS</span></span>

### <span data-ttu-id="eaa96-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="eaa96-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="eaa96-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="eaa96-132">NOTES</span></span>

## <span data-ttu-id="eaa96-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eaa96-133">RELATED LINKS</span></span>
