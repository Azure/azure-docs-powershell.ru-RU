---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 6582b8d0a141522e6ac8bb4dad23f1da5e31000d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914910"
---
# <span data-ttu-id="33bef-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33bef-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="33bef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="33bef-102">SYNOPSIS</span></span>
<span data-ttu-id="33bef-103">Перезапуск VMSS или виртуальной машины в VMSS.</span><span class="sxs-lookup"><span data-stu-id="33bef-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33bef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="33bef-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33bef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33bef-105">DESCRIPTION</span></span>
<span data-ttu-id="33bef-106">Командлет **restarting-AzureRmVmss** перезапустит установленный для виртуальной машины (VMSS).</span><span class="sxs-lookup"><span data-stu-id="33bef-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="33bef-107">Этот командлет также можно использовать для перезапуска определенной виртуальной машины внутри VMSS с помощью параметра *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="33bef-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="33bef-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="33bef-108">EXAMPLES</span></span>

### <span data-ttu-id="33bef-109">Пример 1: перезапуск VMSS</span><span class="sxs-lookup"><span data-stu-id="33bef-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="33bef-110">Эта команда перезапускает VMSS с именем VMSS001, который относится к группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="33bef-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="33bef-111">Пример 2: перезагрузка определенной виртуальной машины в VMSS</span><span class="sxs-lookup"><span data-stu-id="33bef-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="33bef-112">Эта команда перезапускает виртуальную машину с ИДЕНТИФИКАТОРом 1 в VMSS с именем VMSS001, которая входит в группу ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="33bef-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="33bef-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="33bef-113">PARAMETERS</span></span>

### <span data-ttu-id="33bef-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33bef-114">-AsJob</span></span>
<span data-ttu-id="33bef-115">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="33bef-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="33bef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33bef-116">-DefaultProfile</span></span>
<span data-ttu-id="33bef-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="33bef-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33bef-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="33bef-118">-InstanceId</span></span>
<span data-ttu-id="33bef-119">Задает в качестве строкового массива ИДЕНТИФИКАТОРы экземпляров, которые необходимо перезапустить.</span><span class="sxs-lookup"><span data-stu-id="33bef-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33bef-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33bef-120">-ResourceGroupName</span></span>
<span data-ttu-id="33bef-121">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="33bef-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="33bef-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="33bef-122">-VMScaleSetName</span></span>
<span data-ttu-id="33bef-123">Форель имя VMSS, перезапускаемого командлетом.</span><span class="sxs-lookup"><span data-stu-id="33bef-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="33bef-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33bef-124">-Confirm</span></span>
<span data-ttu-id="33bef-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="33bef-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33bef-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33bef-126">-WhatIf</span></span>
<span data-ttu-id="33bef-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="33bef-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33bef-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="33bef-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33bef-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33bef-129">CommonParameters</span></span>
<span data-ttu-id="33bef-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="33bef-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33bef-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33bef-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33bef-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="33bef-132">INPUTS</span></span>

### <span data-ttu-id="33bef-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="33bef-133">None</span></span>
<span data-ttu-id="33bef-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="33bef-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33bef-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33bef-135">OUTPUTS</span></span>

###  
<span data-ttu-id="33bef-136">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="33bef-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="33bef-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="33bef-137">NOTES</span></span>

## <span data-ttu-id="33bef-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33bef-138">RELATED LINKS</span></span>

[<span data-ttu-id="33bef-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33bef-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="33bef-140">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33bef-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="33bef-141">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33bef-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="33bef-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33bef-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="33bef-143">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33bef-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="33bef-144">Остановить-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33bef-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="33bef-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33bef-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


