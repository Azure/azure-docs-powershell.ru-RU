---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: 44022fe8ea12c8f341952bd023aa41bf4ead92c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566290"
---
# <span data-ttu-id="77405-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="77405-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="77405-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77405-102">SYNOPSIS</span></span>
<span data-ttu-id="77405-103">Обновляет состояние VMSS.</span><span class="sxs-lookup"><span data-stu-id="77405-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77405-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77405-104">SYNTAX</span></span>

```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77405-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77405-105">DESCRIPTION</span></span>
<span data-ttu-id="77405-106">Командлет **Update-AzureRmVmss** обновляет состояние набора масштабов виртуальных машин (VMSS) в состояние ЛОКАЛЬНОГО объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="77405-106">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="77405-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77405-107">EXAMPLES</span></span>

### <span data-ttu-id="77405-108">Пример 1: обновление состояния VMSS до состояния локального объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="77405-108">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet "LocalVMSS"
```

<span data-ttu-id="77405-109">Эта команда обновляет состояние VMSS с именем VMSS001, которое принадлежит группе ресурсов с именем Group001, в состояние локального объекта VMSS, именуемого LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="77405-109">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object named LocalVMSS.</span></span>

## <span data-ttu-id="77405-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77405-110">PARAMETERS</span></span>

### <span data-ttu-id="77405-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77405-111">-DefaultProfile</span></span>
<span data-ttu-id="77405-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77405-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77405-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77405-113">-ResourceGroupName</span></span>
<span data-ttu-id="77405-114">Указывает имя группы ресурсов, к которой принадлежит VMSS.</span><span class="sxs-lookup"><span data-stu-id="77405-114">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="77405-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="77405-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="77405-116">Указывает локальный объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="77405-116">Specifies a local VMSS object.</span></span>
<span data-ttu-id="77405-117">Чтобы получить объект VMSS, используйте командлет Get-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="77405-117">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="77405-118">Этот объект виртуальной машины включает обновленное состояние для VMSS.</span><span class="sxs-lookup"><span data-stu-id="77405-118">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77405-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="77405-119">-VMScaleSetName</span></span>
<span data-ttu-id="77405-120">Указывает имя VMSS, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="77405-120">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="77405-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77405-121">-Confirm</span></span>
<span data-ttu-id="77405-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="77405-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77405-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77405-123">-WhatIf</span></span>
<span data-ttu-id="77405-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="77405-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="77405-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="77405-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77405-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77405-126">CommonParameters</span></span>
<span data-ttu-id="77405-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77405-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77405-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77405-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77405-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77405-129">INPUTS</span></span>

## <span data-ttu-id="77405-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77405-130">OUTPUTS</span></span>

## <span data-ttu-id="77405-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="77405-131">NOTES</span></span>

## <span data-ttu-id="77405-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77405-132">RELATED LINKS</span></span>

[<span data-ttu-id="77405-133">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="77405-133">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="77405-134">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="77405-134">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="77405-135">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="77405-135">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="77405-136">Restarting-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="77405-136">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="77405-137">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="77405-137">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="77405-138">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="77405-138">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="77405-139">Остановить-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="77405-139">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


