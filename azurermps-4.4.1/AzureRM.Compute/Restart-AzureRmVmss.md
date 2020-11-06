---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
ms.openlocfilehash: 479aaf61169cb09d8561e9f09b05a5852c93b58d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557848"
---
# <span data-ttu-id="f7874-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f7874-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="f7874-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7874-102">SYNOPSIS</span></span>
<span data-ttu-id="f7874-103">Перезапуск VMSS или виртуальной машины в VMSS.</span><span class="sxs-lookup"><span data-stu-id="f7874-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7874-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7874-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7874-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7874-105">DESCRIPTION</span></span>
<span data-ttu-id="f7874-106">Командлет **restarting-AzureRmVmss** перезапустит установленный для виртуальной машины (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f7874-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="f7874-107">Этот командлет также можно использовать для перезапуска определенной виртуальной машины внутри VMSS с помощью параметра *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="f7874-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="f7874-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7874-108">EXAMPLES</span></span>

### <span data-ttu-id="f7874-109">Пример 1: перезапуск VMSS</span><span class="sxs-lookup"><span data-stu-id="f7874-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="f7874-110">Эта команда перезапускает VMSS с именем VMSS001, который относится к группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="f7874-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="f7874-111">Пример 2: перезагрузка определенной виртуальной машины в VMSS</span><span class="sxs-lookup"><span data-stu-id="f7874-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="f7874-112">Эта команда перезапускает виртуальную машину с ИДЕНТИФИКАТОРом 1 в VMSS с именем VMSS001, которая входит в группу ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="f7874-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="f7874-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7874-113">PARAMETERS</span></span>

### <span data-ttu-id="f7874-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7874-114">-DefaultProfile</span></span>
<span data-ttu-id="f7874-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7874-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7874-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="f7874-116">-InstanceId</span></span>
<span data-ttu-id="f7874-117">Задает в качестве строкового массива ИДЕНТИФИКАТОРы экземпляров, которые необходимо перезапустить.</span><span class="sxs-lookup"><span data-stu-id="f7874-117">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7874-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7874-118">-ResourceGroupName</span></span>
<span data-ttu-id="f7874-119">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="f7874-119">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7874-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f7874-120">-VMScaleSetName</span></span>
<span data-ttu-id="f7874-121">Форель имя VMSS, перезапускаемого командлетом.</span><span class="sxs-lookup"><span data-stu-id="f7874-121">Species the name of the VMSS that this cmdlet restarts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7874-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7874-122">-Confirm</span></span>
<span data-ttu-id="f7874-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7874-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7874-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7874-124">-WhatIf</span></span>
<span data-ttu-id="f7874-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7874-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7874-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7874-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7874-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7874-127">CommonParameters</span></span>
<span data-ttu-id="f7874-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7874-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7874-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7874-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7874-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7874-130">INPUTS</span></span>

## <span data-ttu-id="f7874-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7874-131">OUTPUTS</span></span>

###  
<span data-ttu-id="f7874-132">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f7874-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f7874-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7874-133">NOTES</span></span>

## <span data-ttu-id="f7874-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7874-134">RELATED LINKS</span></span>

[<span data-ttu-id="f7874-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f7874-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="f7874-136">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f7874-136">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="f7874-137">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f7874-137">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="f7874-138">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f7874-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="f7874-139">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f7874-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="f7874-140">Остановить-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f7874-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="f7874-141">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f7874-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


