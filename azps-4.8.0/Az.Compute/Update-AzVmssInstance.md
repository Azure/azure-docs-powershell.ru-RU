---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: f7adb9ef086b233d44f2e5d9c6eb132669b102e5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078104"
---
# <span data-ttu-id="5d838-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="5d838-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="5d838-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d838-102">SYNOPSIS</span></span>
<span data-ttu-id="5d838-103">Запускает обновление экземпляра VMSS вручную.</span><span class="sxs-lookup"><span data-stu-id="5d838-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="5d838-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d838-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d838-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d838-105">DESCRIPTION</span></span>
<span data-ttu-id="5d838-106">Командлет Update-AzVmssInstance запускает ручное обновление указанного экземпляра установленного набора масштаба виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="5d838-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="5d838-107">Этот параметр используется, если для политики обновления в VMSS масштабе задано значение "вручную".</span><span class="sxs-lookup"><span data-stu-id="5d838-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="5d838-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d838-108">EXAMPLES</span></span>

### <span data-ttu-id="5d838-109">Пример 1: Начало обновления экземпляра VMSS</span><span class="sxs-lookup"><span data-stu-id="5d838-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="5d838-110">Эта команда запускает обновление VMSS с именем VMScaleSet001, которое содержит идентификатор экземпляра 0.</span><span class="sxs-lookup"><span data-stu-id="5d838-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="5d838-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d838-111">PARAMETERS</span></span>

### <span data-ttu-id="5d838-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d838-112">-AsJob</span></span>
<span data-ttu-id="5d838-113">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="5d838-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5d838-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d838-114">-DefaultProfile</span></span>
<span data-ttu-id="5d838-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d838-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d838-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="5d838-116">-InstanceId</span></span>
<span data-ttu-id="5d838-117">Задает в качестве строкового массива идентификатор или идентификаторы экземпляра для обновления.</span><span class="sxs-lookup"><span data-stu-id="5d838-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d838-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d838-118">-ResourceGroupName</span></span>
<span data-ttu-id="5d838-119">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="5d838-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="5d838-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5d838-120">-VMScaleSetName</span></span>
<span data-ttu-id="5d838-121">Указывает имя экземпляра VMSS, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5d838-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d838-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d838-122">-Confirm</span></span>
<span data-ttu-id="5d838-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5d838-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d838-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d838-124">-WhatIf</span></span>
<span data-ttu-id="5d838-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5d838-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d838-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5d838-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d838-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d838-127">CommonParameters</span></span>
<span data-ttu-id="5d838-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d838-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d838-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d838-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d838-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d838-130">INPUTS</span></span>

### <span data-ttu-id="5d838-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5d838-131">System.String</span></span>

### <span data-ttu-id="5d838-132">System. String []</span><span class="sxs-lookup"><span data-stu-id="5d838-132">System.String[]</span></span>

## <span data-ttu-id="5d838-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d838-133">OUTPUTS</span></span>

### <span data-ttu-id="5d838-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="5d838-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="5d838-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d838-135">NOTES</span></span>

## <span data-ttu-id="5d838-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d838-136">RELATED LINKS</span></span>

[<span data-ttu-id="5d838-137">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5d838-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


