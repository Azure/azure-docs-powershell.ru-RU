---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVM.md
ms.openlocfilehash: 5a848c2e4a13df6a38c67e067531ff8581bd595e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557852"
---
# <span data-ttu-id="5050f-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5050f-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="5050f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5050f-102">SYNOPSIS</span></span>
<span data-ttu-id="5050f-103">Перезапуск виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="5050f-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5050f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5050f-104">SYNTAX</span></span>

### <span data-ttu-id="5050f-105">RestartResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5050f-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5050f-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="5050f-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5050f-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="5050f-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5050f-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="5050f-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5050f-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5050f-109">DESCRIPTION</span></span>
<span data-ttu-id="5050f-110">Командлет **restart-AzureRmVM** перезапустит виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="5050f-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="5050f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5050f-111">EXAMPLES</span></span>

### <span data-ttu-id="5050f-112">Пример 1: перезапуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="5050f-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="5050f-113">Эта команда перезапускает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5050f-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="5050f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5050f-114">PARAMETERS</span></span>

### <span data-ttu-id="5050f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5050f-115">-DefaultProfile</span></span>
<span data-ttu-id="5050f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5050f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5050f-117">-ID</span><span class="sxs-lookup"><span data-stu-id="5050f-117">-Id</span></span>
<span data-ttu-id="5050f-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5050f-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5050f-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5050f-119">-Name</span></span>
<span data-ttu-id="5050f-120">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5050f-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="5050f-121">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="5050f-121">-PerformMaintenance</span></span>
<span data-ttu-id="5050f-122">Для выполнения обслуживания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5050f-122">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5050f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5050f-123">-ResourceGroupName</span></span>
<span data-ttu-id="5050f-124">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5050f-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5050f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5050f-125">-Confirm</span></span>
<span data-ttu-id="5050f-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5050f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5050f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5050f-127">-WhatIf</span></span>
<span data-ttu-id="5050f-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5050f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5050f-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5050f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5050f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5050f-130">CommonParameters</span></span>
<span data-ttu-id="5050f-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5050f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5050f-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5050f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5050f-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5050f-133">INPUTS</span></span>

## <span data-ttu-id="5050f-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5050f-134">OUTPUTS</span></span>

## <span data-ttu-id="5050f-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="5050f-135">NOTES</span></span>

## <span data-ttu-id="5050f-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5050f-136">RELATED LINKS</span></span>

[<span data-ttu-id="5050f-137">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5050f-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="5050f-138">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5050f-138">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="5050f-139">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5050f-139">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="5050f-140">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5050f-140">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="5050f-141">Остановить-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5050f-141">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="5050f-142">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5050f-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


